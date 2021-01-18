---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504611"
---
# <span data-ttu-id="d58ec-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d58ec-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d58ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d58ec-102">SYNOPSIS</span></span>
<span data-ttu-id="d58ec-103">Добавляет виртуальное правило сети в указанную учетную запись Магазина данных.</span><span class="sxs-lookup"><span data-stu-id="d58ec-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d58ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d58ec-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d58ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d58ec-105">DESCRIPTION</span></span>
<span data-ttu-id="d58ec-106">Командлет **Add-AzDataLakeStoreVirtualNetworkRule** добавляет виртуальное правило сети к указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d58ec-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d58ec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d58ec-107">EXAMPLES</span></span>

### <span data-ttu-id="d58ec-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d58ec-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="d58ec-109">При этом создается новое правило виртуальной сети под названием "myVNET" в учетной записи "dls" с ид подсети testId.</span><span class="sxs-lookup"><span data-stu-id="d58ec-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="d58ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d58ec-110">PARAMETERS</span></span>

### <span data-ttu-id="d58ec-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d58ec-111">-Account</span></span>
<span data-ttu-id="d58ec-112">Учетная запись Магазина данных для добавления виртуального правила сети в</span><span class="sxs-lookup"><span data-stu-id="d58ec-112">The Data Lake Store account to add the virtual network rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58ec-113">-DefaultProfile</span></span>
<span data-ttu-id="d58ec-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d58ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d58ec-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d58ec-115">-Name</span></span>
<span data-ttu-id="d58ec-116">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="d58ec-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58ec-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d58ec-117">-SubnetId</span></span>
<span data-ttu-id="d58ec-118">SubnetId виртуального правила сети</span><span class="sxs-lookup"><span data-stu-id="d58ec-118">The subnetId of the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58ec-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d58ec-119">-Confirm</span></span>
<span data-ttu-id="d58ec-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d58ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58ec-121">-WhatIf</span></span>
<span data-ttu-id="d58ec-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58ec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d58ec-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d58ec-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d58ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58ec-124">CommonParameters</span></span>
<span data-ttu-id="d58ec-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58ec-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58ec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58ec-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d58ec-127">INPUTS</span></span>

### <span data-ttu-id="d58ec-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d58ec-128">System.String</span></span>

## <span data-ttu-id="d58ec-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d58ec-129">OUTPUTS</span></span>

### <span data-ttu-id="d58ec-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d58ec-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d58ec-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d58ec-131">NOTES</span></span>

## <span data-ttu-id="d58ec-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d58ec-132">RELATED LINKS</span></span>
