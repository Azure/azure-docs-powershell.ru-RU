---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250212"
---
# <span data-ttu-id="760d6-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="760d6-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="760d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="760d6-102">SYNOPSIS</span></span>
<span data-ttu-id="760d6-103">Создание объекта, представляющего параметры сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="760d6-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="760d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="760d6-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="760d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="760d6-105">DESCRIPTION</span></span>
<span data-ttu-id="760d6-106">Создание объекта, представляющего параметры сетевого правила, которые можно использовать при создании хранилища.</span><span class="sxs-lookup"><span data-stu-id="760d6-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="760d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="760d6-107">EXAMPLES</span></span>

### <span data-ttu-id="760d6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="760d6-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="760d6-109">Создание нового хранилища и определение сетевых правил, разрешающих доступ к указанному IP-адресу из виртуальной сети, определенной $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="760d6-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="760d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="760d6-110">PARAMETERS</span></span>

### <span data-ttu-id="760d6-111">-Обход</span><span class="sxs-lookup"><span data-stu-id="760d6-111">-Bypass</span></span>
<span data-ttu-id="760d6-112">Указывает обход сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="760d6-112">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="760d6-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="760d6-113">-DefaultAction</span></span>
<span data-ttu-id="760d6-114">Задает действие по умолчанию для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="760d6-114">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="760d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="760d6-115">-DefaultProfile</span></span>
<span data-ttu-id="760d6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="760d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="760d6-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="760d6-117">-IpAddressRange</span></span>
<span data-ttu-id="760d6-118">Указывает допустимый диапазон IP-адресов сети сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="760d6-118">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="760d6-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="760d6-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="760d6-120">Указывает допустимый идентификатор ресурса виртуальной сети для сетевого правила.</span><span class="sxs-lookup"><span data-stu-id="760d6-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="760d6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="760d6-121">CommonParameters</span></span>
<span data-ttu-id="760d6-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="760d6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="760d6-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="760d6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="760d6-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="760d6-124">INPUTS</span></span>

### <span data-ttu-id="760d6-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="760d6-125">None</span></span>

## <span data-ttu-id="760d6-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="760d6-126">OUTPUTS</span></span>

### <span data-ttu-id="760d6-127">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="760d6-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="760d6-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="760d6-128">NOTES</span></span>

## <span data-ttu-id="760d6-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="760d6-129">RELATED LINKS</span></span>
