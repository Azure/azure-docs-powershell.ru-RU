---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326707"
---
# <span data-ttu-id="087a3-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="087a3-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="087a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="087a3-102">SYNOPSIS</span></span>
<span data-ttu-id="087a3-103">Получает настройку закрытой ссылки для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="087a3-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="087a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="087a3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="087a3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="087a3-105">DESCRIPTION</span></span>
<span data-ttu-id="087a3-106">Для шлюза приложения будет отображена конфигурация закрытой ссылки на **веб-часть Get-AzApplicationGatewayPrivateLinkConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="087a3-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="087a3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="087a3-107">EXAMPLES</span></span>

### <span data-ttu-id="087a3-108">Пример 1. Настройка личных ссылок</span><span class="sxs-lookup"><span data-stu-id="087a3-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="087a3-109">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="087a3-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="087a3-110">Вторая команда получает конфигурацию частной ссылки privateLinkConfig01 из $AppGw и сохраняет ее в переменной $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="087a3-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="087a3-111">Пример 2. Получить список настройки закрытой ссылки</span><span class="sxs-lookup"><span data-stu-id="087a3-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="087a3-112">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="087a3-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="087a3-113">Вторая команда получает все параметры личных ссылок из $AppGw и сохраняет их в переменной $PrivateLinkConfigurations.</span><span class="sxs-lookup"><span data-stu-id="087a3-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="087a3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="087a3-114">PARAMETERS</span></span>

### <span data-ttu-id="087a3-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="087a3-115">-ApplicationGateway</span></span>
<span data-ttu-id="087a3-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="087a3-116">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="087a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087a3-117">-DefaultProfile</span></span>
<span data-ttu-id="087a3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="087a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087a3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="087a3-119">-Name</span></span>
<span data-ttu-id="087a3-120">Имя конфигурации PrivateLink шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="087a3-120">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087a3-121">CommonParameters</span></span>
<span data-ttu-id="087a3-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="087a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087a3-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="087a3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087a3-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="087a3-124">INPUTS</span></span>

### <span data-ttu-id="087a3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="087a3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="087a3-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="087a3-126">OUTPUTS</span></span>

### <span data-ttu-id="087a3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="087a3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="087a3-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="087a3-128">NOTES</span></span>

## <span data-ttu-id="087a3-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="087a3-129">RELATED LINKS</span></span>

[<span data-ttu-id="087a3-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="087a3-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="087a3-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="087a3-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="087a3-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="087a3-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="087a3-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="087a3-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)