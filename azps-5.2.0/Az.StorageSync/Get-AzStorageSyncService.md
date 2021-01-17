---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414620"
---
# <span data-ttu-id="0a88c-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0a88c-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="0a88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a88c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a88c-103">Эта команда содержит список всех служб синхронизации хранилища в рамках группы подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a88c-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="0a88c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a88c-104">SYNTAX</span></span>

### <span data-ttu-id="0a88c-105">ParentStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a88c-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a88c-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a88c-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a88c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a88c-107">DESCRIPTION</span></span>
<span data-ttu-id="0a88c-108">Эта команда содержит список всех служб синхронизации хранилища в рамках группы подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a88c-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="0a88c-109">Его также можно использовать для списка атрибутов каждой службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="0a88c-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="0a88c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a88c-110">EXAMPLES</span></span>

### <span data-ttu-id="0a88c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a88c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="0a88c-112">Эта команда содержит список всех ресурсов службы синхронизации хранилища в пределах данной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a88c-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="0a88c-113">Его также можно использовать для списка атрибутов каждой службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="0a88c-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="0a88c-114">Укажите -StorageSyncServiceName, чтобы вернуть определенное имя.</span><span class="sxs-lookup"><span data-stu-id="0a88c-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="0a88c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a88c-115">PARAMETERS</span></span>

### <span data-ttu-id="0a88c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a88c-116">-DefaultProfile</span></span>
<span data-ttu-id="0a88c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a88c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a88c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0a88c-118">-Name</span></span>
<span data-ttu-id="0a88c-119">Имя службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="0a88c-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="0a88c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a88c-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a88c-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a88c-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="0a88c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a88c-122">CommonParameters</span></span>
<span data-ttu-id="0a88c-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a88c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a88c-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a88c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a88c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a88c-125">INPUTS</span></span>

### <span data-ttu-id="0a88c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0a88c-126">System.String</span></span>

## <span data-ttu-id="0a88c-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a88c-127">OUTPUTS</span></span>

### <span data-ttu-id="0a88c-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0a88c-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="0a88c-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a88c-129">NOTES</span></span>

## <span data-ttu-id="0a88c-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a88c-130">RELATED LINKS</span></span>
