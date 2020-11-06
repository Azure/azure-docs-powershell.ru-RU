---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1b404a42c3d40138408d7fb6f2c13a8af91c45c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560916"
---
# <span data-ttu-id="e548a-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e548a-101">Get-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e548a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e548a-102">SYNOPSIS</span></span>
<span data-ttu-id="e548a-103">Получает указанные правила виртуальной сети в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e548a-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e548a-104">Если правило для виртуальной сети не задано, выводится список всех правил для учетной записи в сети.</span><span class="sxs-lookup"><span data-stu-id="e548a-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e548a-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e548a-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e548a-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e548a-106">DESCRIPTION</span></span>
<span data-ttu-id="e548a-107">Командлет Get-AzureRmDataLakeStoreVirtualNetworkRule получает указанные правила для виртуальных сетей в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e548a-107">The Get-AzureRmDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e548a-108">Если правило для виртуальной сети не задано, выводится список всех правил для учетной записи в сети.</span><span class="sxs-lookup"><span data-stu-id="e548a-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="e548a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e548a-109">EXAMPLES</span></span>

### <span data-ttu-id="e548a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e548a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="e548a-111">Возвращает правило виртуальной сети с именем "myVNET" из учетной записи "списки рассылки".</span><span class="sxs-lookup"><span data-stu-id="e548a-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="e548a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e548a-112">PARAMETERS</span></span>

### <span data-ttu-id="e548a-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="e548a-113">-Account</span></span>
<span data-ttu-id="e548a-114">Учетная запись Data Lake Store, из которой нужно получить правило для виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e548a-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="e548a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e548a-115">-DefaultProfile</span></span>
<span data-ttu-id="e548a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e548a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e548a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e548a-117">-Name</span></span>
<span data-ttu-id="e548a-118">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e548a-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="e548a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e548a-119">CommonParameters</span></span>
<span data-ttu-id="e548a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e548a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e548a-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e548a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e548a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e548a-122">INPUTS</span></span>

### <span data-ttu-id="e548a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e548a-123">System.String</span></span>

## <span data-ttu-id="e548a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e548a-124">OUTPUTS</span></span>

### <span data-ttu-id="e548a-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e548a-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="e548a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e548a-126">NOTES</span></span>

## <span data-ttu-id="e548a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e548a-127">RELATED LINKS</span></span>
