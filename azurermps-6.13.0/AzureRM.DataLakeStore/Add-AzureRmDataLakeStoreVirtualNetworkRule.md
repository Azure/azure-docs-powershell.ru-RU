---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: a25125b8aa76fa8d2be99f7f80b8fea2383bdf02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566491"
---
# <span data-ttu-id="d47d1-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d47d1-101">Add-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d47d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d47d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d47d1-103">Добавляет правило виртуальной сети к указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d47d1-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d47d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d47d1-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d47d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d47d1-105">DESCRIPTION</span></span>
<span data-ttu-id="d47d1-106">Командлет **Add-AzureRmDataLakeStoreVirtualNetworkRule** добавляет правило для виртуальной сети в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d47d1-106">The **Add-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d47d1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d47d1-107">EXAMPLES</span></span>

### <span data-ttu-id="d47d1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d47d1-108">Example 1</span></span>
```powershell
PS C:\> Add-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="d47d1-109">Это создаст новое правило виртуальной сети "myVNET" в учетной записи "списки рассылки" с идентификатором подсети "testId"</span><span class="sxs-lookup"><span data-stu-id="d47d1-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="d47d1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d47d1-110">PARAMETERS</span></span>

### <span data-ttu-id="d47d1-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d47d1-111">-Account</span></span>
<span data-ttu-id="d47d1-112">Учетная запись Data Lake Store, к которой нужно добавить правило для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d47d1-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="d47d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d47d1-113">-DefaultProfile</span></span>
<span data-ttu-id="d47d1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d47d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d47d1-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d47d1-115">-Name</span></span>
<span data-ttu-id="d47d1-116">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d47d1-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="d47d1-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d47d1-117">-SubnetId</span></span>
<span data-ttu-id="d47d1-118">SubnetId правила для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d47d1-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="d47d1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d47d1-119">-Confirm</span></span>
<span data-ttu-id="d47d1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d47d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d47d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d47d1-121">-WhatIf</span></span>
<span data-ttu-id="d47d1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d47d1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d47d1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d47d1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d47d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d47d1-124">CommonParameters</span></span>
<span data-ttu-id="d47d1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d47d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d47d1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d47d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d47d1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d47d1-127">INPUTS</span></span>

### <span data-ttu-id="d47d1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d47d1-128">System.String</span></span>

## <span data-ttu-id="d47d1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d47d1-129">OUTPUTS</span></span>

### <span data-ttu-id="d47d1-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d47d1-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="d47d1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d47d1-131">NOTES</span></span>

## <span data-ttu-id="d47d1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d47d1-132">RELATED LINKS</span></span>
