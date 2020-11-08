---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075020"
---
# <span data-ttu-id="7d8de-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7d8de-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="7d8de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d8de-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8de-103">Изменяет указанное правило виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d8de-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7d8de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d8de-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d8de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8de-105">DESCRIPTION</span></span>
<span data-ttu-id="7d8de-106">Командлет **Set-AzDataLakeStoreVirtualNetworkRule** изменяет указанное правило виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d8de-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="7d8de-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d8de-107">EXAMPLES</span></span>

### <span data-ttu-id="7d8de-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d8de-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="7d8de-109">Обновление идентификатора подсети правила виртуальной сети "myVNET" в учетной записи "списки рассылки" на "updatedId"</span><span class="sxs-lookup"><span data-stu-id="7d8de-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="7d8de-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d8de-110">PARAMETERS</span></span>

### <span data-ttu-id="7d8de-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7d8de-111">-Account</span></span>
<span data-ttu-id="7d8de-112">Учетная запись Data Lake Store для обновления правила виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7d8de-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="7d8de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8de-113">-DefaultProfile</span></span>
<span data-ttu-id="7d8de-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d8de-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d8de-115">-Name</span></span>
<span data-ttu-id="7d8de-116">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7d8de-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="7d8de-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="7d8de-117">-SubnetId</span></span>
<span data-ttu-id="7d8de-118">Начало диапазона допустимых IP-адресов для правила виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7d8de-118">The start of the valid ip range for the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d8de-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d8de-119">-Confirm</span></span>
<span data-ttu-id="7d8de-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d8de-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8de-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8de-121">-WhatIf</span></span>
<span data-ttu-id="7d8de-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d8de-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8de-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d8de-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8de-124">CommonParameters</span></span>
<span data-ttu-id="7d8de-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d8de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8de-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8de-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8de-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d8de-127">INPUTS</span></span>

### <span data-ttu-id="7d8de-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7d8de-128">System.String</span></span>

## <span data-ttu-id="7d8de-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d8de-129">OUTPUTS</span></span>

### <span data-ttu-id="7d8de-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7d8de-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="7d8de-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d8de-131">NOTES</span></span>

## <span data-ttu-id="7d8de-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d8de-132">RELATED LINKS</span></span>
