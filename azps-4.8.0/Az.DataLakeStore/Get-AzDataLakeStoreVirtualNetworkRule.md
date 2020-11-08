---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235595"
---
# <span data-ttu-id="b3eca-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b3eca-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b3eca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3eca-102">SYNOPSIS</span></span>
<span data-ttu-id="b3eca-103">Получает указанные правила виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b3eca-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b3eca-104">Если правило для виртуальной сети не задано, выводится список всех правил для учетной записи в сети.</span><span class="sxs-lookup"><span data-stu-id="b3eca-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="b3eca-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3eca-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3eca-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3eca-106">DESCRIPTION</span></span>
<span data-ttu-id="b3eca-107">Командлет Get-AzDataLakeStoreVirtualNetworkRule получает указанные правила для виртуальных сетей в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b3eca-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="b3eca-108">Если правило для виртуальной сети не задано, выводится список всех правил для учетной записи в сети.</span><span class="sxs-lookup"><span data-stu-id="b3eca-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="b3eca-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3eca-109">EXAMPLES</span></span>

### <span data-ttu-id="b3eca-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3eca-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="b3eca-111">Возвращает правило виртуальной сети с именем "myVNET" из учетной записи "списки рассылки".</span><span class="sxs-lookup"><span data-stu-id="b3eca-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="b3eca-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3eca-112">PARAMETERS</span></span>

### <span data-ttu-id="b3eca-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b3eca-113">-Account</span></span>
<span data-ttu-id="b3eca-114">Учетная запись Data Lake Store, из которой нужно получить правило для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b3eca-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="b3eca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3eca-115">-DefaultProfile</span></span>
<span data-ttu-id="b3eca-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3eca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3eca-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3eca-117">-Name</span></span>
<span data-ttu-id="b3eca-118">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b3eca-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b3eca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3eca-119">CommonParameters</span></span>
<span data-ttu-id="b3eca-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3eca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3eca-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3eca-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3eca-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3eca-122">INPUTS</span></span>

### <span data-ttu-id="b3eca-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b3eca-123">System.String</span></span>

## <span data-ttu-id="b3eca-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3eca-124">OUTPUTS</span></span>

### <span data-ttu-id="b3eca-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b3eca-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b3eca-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3eca-126">NOTES</span></span>

## <span data-ttu-id="b3eca-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3eca-127">RELATED LINKS</span></span>
