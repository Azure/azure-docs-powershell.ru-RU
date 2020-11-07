---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: 9eca6930caccd2796362e32f1617ee98bcda0885
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907502"
---
# <span data-ttu-id="bafff-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bafff-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="bafff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bafff-102">SYNOPSIS</span></span>
<span data-ttu-id="bafff-103">Эта команда выводит список всех служб синхронизации хранилища в заданной области подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bafff-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="bafff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bafff-104">SYNTAX</span></span>

### <span data-ttu-id="bafff-105">ParentStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bafff-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bafff-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bafff-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bafff-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bafff-107">DESCRIPTION</span></span>
<span data-ttu-id="bafff-108">Эта команда выводит список всех служб синхронизации хранилища в заданной области подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bafff-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="bafff-109">Он также может использоваться для перечисления атрибутов каждой службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="bafff-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="bafff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bafff-110">EXAMPLES</span></span>

### <span data-ttu-id="bafff-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bafff-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="bafff-112">Эта команда выводит список всех ресурсов службы синхронизации хранилища в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bafff-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="bafff-113">Он также может использоваться для перечисления атрибутов каждой службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="bafff-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="bafff-114">Укажите-StorageSyncServiceName, чтобы вернуть определенную единицу.</span><span class="sxs-lookup"><span data-stu-id="bafff-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="bafff-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bafff-115">PARAMETERS</span></span>

### <span data-ttu-id="bafff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafff-116">-DefaultProfile</span></span>
<span data-ttu-id="bafff-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bafff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bafff-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bafff-118">-Name</span></span>
<span data-ttu-id="bafff-119">Имя службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="bafff-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafff-120">-ResourceGroupName</span></span>
<span data-ttu-id="bafff-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bafff-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafff-122">CommonParameters</span></span>
<span data-ttu-id="bafff-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bafff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafff-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bafff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafff-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bafff-125">INPUTS</span></span>

### <span data-ttu-id="bafff-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bafff-126">System.String</span></span>

## <span data-ttu-id="bafff-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bafff-127">OUTPUTS</span></span>

### <span data-ttu-id="bafff-128">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bafff-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="bafff-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="bafff-129">NOTES</span></span>

## <span data-ttu-id="bafff-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bafff-130">RELATED LINKS</span></span>
