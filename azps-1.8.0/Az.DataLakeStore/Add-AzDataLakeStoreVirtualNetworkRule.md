---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 4fccc705951ba944afdf13bf75d581e7c76d593f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731077"
---
# <span data-ttu-id="e2d0f-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e2d0f-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e2d0f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d0f-103">Добавляет правило виртуальной сети к указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="e2d0f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2d0f-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d0f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d0f-106">Командлет **Add-AzDataLakeStoreVirtualNetworkRule** добавляет правило для виртуальной сети в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="e2d0f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2d0f-107">EXAMPLES</span></span>

### <span data-ttu-id="e2d0f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2d0f-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="e2d0f-109">Это создаст новое правило виртуальной сети "myVNET" в учетной записи "списки рассылки" с идентификатором подсети "testId"</span><span class="sxs-lookup"><span data-stu-id="e2d0f-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="e2d0f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2d0f-110">PARAMETERS</span></span>

### <span data-ttu-id="e2d0f-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-111">-Account</span></span>
<span data-ttu-id="e2d0f-112">Учетная запись Data Lake Store, к которой нужно добавить правило для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e2d0f-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="e2d0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d0f-113">-DefaultProfile</span></span>
<span data-ttu-id="e2d0f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2d0f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2d0f-115">-Name</span></span>
<span data-ttu-id="e2d0f-116">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e2d0f-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e2d0f-117">-SubnetId</span></span>
<span data-ttu-id="e2d0f-118">SubnetId правила для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e2d0f-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="e2d0f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2d0f-119">-Confirm</span></span>
<span data-ttu-id="e2d0f-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2d0f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d0f-121">-WhatIf</span></span>
<span data-ttu-id="e2d0f-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d0f-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2d0f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d0f-124">CommonParameters</span></span>
<span data-ttu-id="e2d0f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2d0f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d0f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d0f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d0f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2d0f-127">INPUTS</span></span>

### <span data-ttu-id="e2d0f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e2d0f-128">System.String</span></span>

## <span data-ttu-id="e2d0f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2d0f-129">OUTPUTS</span></span>

### <span data-ttu-id="e2d0f-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e2d0f-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e2d0f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2d0f-131">NOTES</span></span>

## <span data-ttu-id="e2d0f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2d0f-132">RELATED LINKS</span></span>
