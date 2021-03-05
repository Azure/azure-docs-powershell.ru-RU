---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 957417d7751080a82ddc8785abdd124c8f723303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003608"
---
# <span data-ttu-id="9ab8a-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ab8a-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="9ab8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ab8a-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab8a-103">Получает back-end HTTP-параметры шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="9ab8a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ab8a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ab8a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ab8a-105">DESCRIPTION</span></span>
<span data-ttu-id="9ab8a-106">С Get-AzApplicationGatewayBackendHttpSetting- и HTTP-параметры шлюза приложения получаются дополнительные параметры HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="9ab8a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ab8a-107">EXAMPLES</span></span>

### <span data-ttu-id="9ab8a-108">Пример 1. Создание back-end HTTP-параметров по имени</span><span class="sxs-lookup"><span data-stu-id="9ab8a-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="9ab8a-109">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной. Вторая команда получает параметры HTTP с именем "Параметры01 для $AppGw и сохраняет их в $Settings переменной.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="9ab8a-110">Пример 2. Получить набор конечных параметров HTTP</span><span class="sxs-lookup"><span data-stu-id="9ab8a-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="9ab8a-111">Первая команда получает шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01 и сохраняет его в $AppGw переменной. Вторая команда получает набор параметров HTTP для $AppGw и сохраняет их в переменной $SettingsList http.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="9ab8a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ab8a-112">PARAMETERS</span></span>

### <span data-ttu-id="9ab8a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ab8a-113">-ApplicationGateway</span></span>
<span data-ttu-id="9ab8a-114">Определяет объект шлюза приложения, который содержит back-end HTTP-параметры.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ab8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab8a-115">-DefaultProfile</span></span>
<span data-ttu-id="9ab8a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab8a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ab8a-117">-Name</span></span>
<span data-ttu-id="9ab8a-118">Определяет имя параметров HTTP-адреса, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab8a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab8a-119">CommonParameters</span></span>
<span data-ttu-id="9ab8a-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab8a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab8a-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ab8a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab8a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ab8a-122">INPUTS</span></span>

### <span data-ttu-id="9ab8a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ab8a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ab8a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ab8a-124">OUTPUTS</span></span>

### <span data-ttu-id="9ab8a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9ab8a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="9ab8a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ab8a-126">NOTES</span></span>

## <span data-ttu-id="9ab8a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ab8a-127">RELATED LINKS</span></span>

[<span data-ttu-id="9ab8a-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ab8a-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9ab8a-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ab8a-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9ab8a-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ab8a-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="9ab8a-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="9ab8a-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

