---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: d3f774b078c1069fc5a2c2690996837f17a4c187
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994101"
---
# <span data-ttu-id="07283-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="07283-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="07283-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07283-102">SYNOPSIS</span></span>
<span data-ttu-id="07283-103">Получает настройку закрытой ссылки для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="07283-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="07283-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07283-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07283-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07283-105">DESCRIPTION</span></span>
<span data-ttu-id="07283-106">Для шлюза приложения будет отображена конфигурация закрытой ссылки для **get-AzApplicationGatewayPrivateLinkConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="07283-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="07283-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07283-107">EXAMPLES</span></span>

### <span data-ttu-id="07283-108">Пример 1. Настройка личных ссылок</span><span class="sxs-lookup"><span data-stu-id="07283-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="07283-109">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="07283-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="07283-110">Вторая команда получает от имени privateLinkConfig01 конфигурацию privateLinkConfig01 из $AppGw и сохраняет ее в переменной $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="07283-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="07283-111">Пример 2. Получить список настройки закрытой ссылки</span><span class="sxs-lookup"><span data-stu-id="07283-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="07283-112">Первая команда получает шлюз приложения ApplicationGateway01 из группы ресурсов ResourceGroup01 и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="07283-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="07283-113">Вторая команда получает все параметры личных ссылок из $AppGw и сохраняет их в переменной $PrivateLinkConfigurations.</span><span class="sxs-lookup"><span data-stu-id="07283-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="07283-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07283-114">PARAMETERS</span></span>

### <span data-ttu-id="07283-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07283-115">-ApplicationGateway</span></span>
<span data-ttu-id="07283-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07283-116">The applicationGateway</span></span>

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

### <span data-ttu-id="07283-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07283-117">-DefaultProfile</span></span>
<span data-ttu-id="07283-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07283-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07283-119">-Name</span><span class="sxs-lookup"><span data-stu-id="07283-119">-Name</span></span>
<span data-ttu-id="07283-120">Имя конфигурации PrivateLink шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="07283-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="07283-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07283-121">CommonParameters</span></span>
<span data-ttu-id="07283-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07283-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07283-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07283-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07283-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07283-124">INPUTS</span></span>

### <span data-ttu-id="07283-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07283-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="07283-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07283-126">OUTPUTS</span></span>

### <span data-ttu-id="07283-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="07283-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="07283-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07283-128">NOTES</span></span>

## <span data-ttu-id="07283-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07283-129">RELATED LINKS</span></span>

[<span data-ttu-id="07283-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="07283-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="07283-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="07283-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="07283-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="07283-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="07283-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="07283-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)