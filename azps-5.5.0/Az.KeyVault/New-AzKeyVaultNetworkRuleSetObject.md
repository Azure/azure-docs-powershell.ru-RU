---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219612"
---
# <span data-ttu-id="3ae74-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="3ae74-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="3ae74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ae74-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae74-103">Создание объекта, представляющего параметры правил сети.</span><span class="sxs-lookup"><span data-stu-id="3ae74-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="3ae74-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3ae74-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ae74-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ae74-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae74-106">Создание объекта, представляющего параметры правил сети, которые можно использовать при создании сейфа.</span><span class="sxs-lookup"><span data-stu-id="3ae74-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="3ae74-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3ae74-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae74-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ae74-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="3ae74-109">Создание нового хранилища и определяет правила сети, позволяющие получить доступ к указанному IP-адресу из виртуальной сети, указанной $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="3ae74-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="3ae74-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ae74-110">PARAMETERS</span></span>

### <span data-ttu-id="3ae74-111">-Bypass</span><span class="sxs-lookup"><span data-stu-id="3ae74-111">-Bypass</span></span>
<span data-ttu-id="3ae74-112">Определяет обход правила сети.</span><span class="sxs-lookup"><span data-stu-id="3ae74-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae74-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="3ae74-113">-DefaultAction</span></span>
<span data-ttu-id="3ae74-114">Указывает действие по умолчанию для правила сети.</span><span class="sxs-lookup"><span data-stu-id="3ae74-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae74-115">-DefaultProfile</span></span>
<span data-ttu-id="3ae74-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae74-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae74-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="3ae74-117">-IpAddressRange</span></span>
<span data-ttu-id="3ae74-118">Диапазон разрешенных IP-адресов сети для правила сети.</span><span class="sxs-lookup"><span data-stu-id="3ae74-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae74-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3ae74-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3ae74-120">Определяет допустимый идентификатор виртуального сетевого ресурса для правила сети.</span><span class="sxs-lookup"><span data-stu-id="3ae74-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae74-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae74-121">CommonParameters</span></span>
<span data-ttu-id="3ae74-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae74-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae74-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ae74-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae74-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ae74-124">INPUTS</span></span>

### <span data-ttu-id="3ae74-125">Нет</span><span class="sxs-lookup"><span data-stu-id="3ae74-125">None</span></span>

## <span data-ttu-id="3ae74-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ae74-126">OUTPUTS</span></span>

### <span data-ttu-id="3ae74-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3ae74-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="3ae74-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3ae74-128">NOTES</span></span>

## <span data-ttu-id="3ae74-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ae74-129">RELATED LINKS</span></span>
