---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912120"
---
# <span data-ttu-id="fb230-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="fb230-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="fb230-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb230-102">SYNOPSIS</span></span>
<span data-ttu-id="fb230-103">Эта команда выводит список всех служб синхронизации хранилища в заданной области подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb230-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="fb230-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb230-104">SYNTAX</span></span>

### <span data-ttu-id="fb230-105">ParentStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb230-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb230-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb230-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb230-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb230-107">DESCRIPTION</span></span>
<span data-ttu-id="fb230-108">Эта команда выводит список всех служб синхронизации хранилища в заданной области подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb230-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="fb230-109">Он также может использоваться для перечисления атрибутов каждой службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="fb230-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="fb230-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb230-110">EXAMPLES</span></span>

### <span data-ttu-id="fb230-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb230-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="fb230-112">Эта команда выводит список всех ресурсов службы синхронизации хранилища в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb230-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="fb230-113">Он также может использоваться для перечисления атрибутов каждой службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="fb230-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="fb230-114">Укажите-StorageSyncServiceName, чтобы вернуть определенную единицу.</span><span class="sxs-lookup"><span data-stu-id="fb230-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="fb230-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb230-115">PARAMETERS</span></span>

### <span data-ttu-id="fb230-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb230-116">-DefaultProfile</span></span>
<span data-ttu-id="fb230-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb230-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb230-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb230-118">-Name</span></span>
<span data-ttu-id="fb230-119">Имя службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="fb230-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="fb230-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb230-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb230-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb230-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb230-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb230-122">CommonParameters</span></span>
<span data-ttu-id="fb230-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb230-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb230-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb230-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb230-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb230-125">INPUTS</span></span>

### <span data-ttu-id="fb230-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fb230-126">System.String</span></span>

## <span data-ttu-id="fb230-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb230-127">OUTPUTS</span></span>

### <span data-ttu-id="fb230-128">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="fb230-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="fb230-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb230-129">NOTES</span></span>

## <span data-ttu-id="fb230-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb230-130">RELATED LINKS</span></span>
