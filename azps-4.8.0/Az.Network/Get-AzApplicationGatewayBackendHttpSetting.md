---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079498"
---
# <span data-ttu-id="7f6d5-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7f6d5-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="7f6d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6d5-103">Получает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7f6d5-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="7f6d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f6d5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f6d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f6d5-105">DESCRIPTION</span></span>
<span data-ttu-id="7f6d5-106">Командлет Get-AzApplicationGatewayBackendHttpSetting получает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7f6d5-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="7f6d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f6d5-107">EXAMPLES</span></span>

### <span data-ttu-id="7f6d5-108">Пример 1: получение HTTP-параметров "на сервер" по имени</span><span class="sxs-lookup"><span data-stu-id="7f6d5-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7f6d5-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда получает параметры HTTP с именем Settings01 для $AppGw и сохраняет параметры в переменной $Settings.</span><span class="sxs-lookup"><span data-stu-id="7f6d5-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="7f6d5-110">Пример 2: получение коллекции параметров HTTP для веб-части</span><span class="sxs-lookup"><span data-stu-id="7f6d5-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="7f6d5-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет ее в переменной $AppGw. Вторая команда получает коллекцию параметров HTTP для $AppGw и сохраняет параметры в переменной $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="7f6d5-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="7f6d5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f6d5-112">PARAMETERS</span></span>

### <span data-ttu-id="7f6d5-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f6d5-113">-ApplicationGateway</span></span>
<span data-ttu-id="7f6d5-114">Указывает объект шлюза приложения, который содержит параметры HTTP для внутренней стороны.</span><span class="sxs-lookup"><span data-stu-id="7f6d5-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="7f6d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6d5-115">-DefaultProfile</span></span>
<span data-ttu-id="7f6d5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6d5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f6d5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f6d5-117">-Name</span></span>
<span data-ttu-id="7f6d5-118">Указывает имя HTTP-параметров серверной части, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7f6d5-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7f6d5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6d5-119">CommonParameters</span></span>
<span data-ttu-id="7f6d5-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f6d5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6d5-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f6d5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6d5-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f6d5-122">INPUTS</span></span>

### <span data-ttu-id="7f6d5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f6d5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f6d5-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f6d5-124">OUTPUTS</span></span>

### <span data-ttu-id="7f6d5-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7f6d5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7f6d5-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f6d5-126">NOTES</span></span>

## <span data-ttu-id="7f6d5-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f6d5-127">RELATED LINKS</span></span>

[<span data-ttu-id="7f6d5-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7f6d5-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7f6d5-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7f6d5-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7f6d5-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7f6d5-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7f6d5-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7f6d5-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

