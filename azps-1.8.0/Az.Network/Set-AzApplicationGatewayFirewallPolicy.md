---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730060"
---
# <span data-ttu-id="e1f92-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e1f92-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="e1f92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1f92-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f92-103">Обновляет политику брандмауэра для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e1f92-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="e1f92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1f92-104">SYNTAX</span></span>

### <span data-ttu-id="e1f92-105">ByFactoryObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1f92-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f92-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="e1f92-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f92-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1f92-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1f92-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f92-108">DESCRIPTION</span></span>
<span data-ttu-id="e1f92-109">Командлет **Set-AzApplicationGatewayFirewallPolicy** обновляет политику брандмауэра для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f92-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="e1f92-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1f92-110">EXAMPLES</span></span>

### <span data-ttu-id="e1f92-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1f92-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="e1f92-112">Эта команда обновляет политику брандмауэра для шлюза приложений с помощью параметров в переменной $AppGwFirewallPolicy и сохраняет обновленный шлюз в переменной $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="e1f92-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="e1f92-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1f92-113">PARAMETERS</span></span>

### <span data-ttu-id="e1f92-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1f92-114">-AsJob</span></span>
<span data-ttu-id="e1f92-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e1f92-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f92-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="e1f92-116">-CustomRule</span></span>
<span data-ttu-id="e1f92-117">Список CustomRules</span><span class="sxs-lookup"><span data-stu-id="e1f92-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f92-118">-DefaultProfile</span></span>
<span data-ttu-id="e1f92-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f92-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1f92-120">-InputObject</span></span>
<span data-ttu-id="e1f92-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e1f92-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f92-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1f92-122">-Name</span></span>
<span data-ttu-id="e1f92-123">Имя политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e1f92-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f92-124">-ResourceGroupName</span></span>
<span data-ttu-id="e1f92-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1f92-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f92-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1f92-126">-ResourceId</span></span>
<span data-ttu-id="e1f92-127">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f92-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f92-128">CommonParameters</span></span>
<span data-ttu-id="e1f92-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1f92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f92-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f92-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f92-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1f92-131">INPUTS</span></span>

### <span data-ttu-id="e1f92-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e1f92-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="e1f92-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f92-133">OUTPUTS</span></span>

### <span data-ttu-id="e1f92-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e1f92-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="e1f92-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1f92-135">NOTES</span></span>

## <span data-ttu-id="e1f92-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1f92-136">RELATED LINKS</span></span>
