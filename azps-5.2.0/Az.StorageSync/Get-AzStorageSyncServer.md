---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414636"
---
# <span data-ttu-id="50f77-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="50f77-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="50f77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f77-102">SYNOPSIS</span></span>
<span data-ttu-id="50f77-103">Эта команда содержит список всех серверов, зарегистрированных в данной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="50f77-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="50f77-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50f77-104">SYNTAX</span></span>

### <span data-ttu-id="50f77-105">StringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50f77-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50f77-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f77-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50f77-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f77-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50f77-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50f77-108">DESCRIPTION</span></span>
<span data-ttu-id="50f77-109">Эта команда содержит список всех серверов, зарегистрированных в данной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="50f77-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="50f77-110">Его также можно использовать для списка атрибутов каждого зарегистрированного сервера.</span><span class="sxs-lookup"><span data-stu-id="50f77-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="50f77-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50f77-111">EXAMPLES</span></span>

### <span data-ttu-id="50f77-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50f77-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="50f77-113">Эта команда возвращает все серверы, зарегистрированные в определенной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="50f77-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="50f77-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50f77-114">PARAMETERS</span></span>

### <span data-ttu-id="50f77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f77-115">-DefaultProfile</span></span>
<span data-ttu-id="50f77-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50f77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50f77-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="50f77-117">-ParentObject</span></span>
<span data-ttu-id="50f77-118">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="50f77-118">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50f77-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="50f77-119">-ParentResourceId</span></span>
<span data-ttu-id="50f77-120">Объект StorageSyncService, обычно переданный через параметр.</span><span class="sxs-lookup"><span data-stu-id="50f77-120">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50f77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f77-121">-ResourceGroupName</span></span>
<span data-ttu-id="50f77-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50f77-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="50f77-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="50f77-123">-ServerId</span></span>
<span data-ttu-id="50f77-124">Имя зарегистрированногоServer.</span><span class="sxs-lookup"><span data-stu-id="50f77-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50f77-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="50f77-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="50f77-126">Имя службы StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="50f77-126">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50f77-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f77-127">CommonParameters</span></span>
<span data-ttu-id="50f77-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f77-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f77-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f77-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f77-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50f77-130">INPUTS</span></span>

### <span data-ttu-id="50f77-131">System.String</span><span class="sxs-lookup"><span data-stu-id="50f77-131">System.String</span></span>

### <span data-ttu-id="50f77-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="50f77-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="50f77-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="50f77-133">System.Guid</span></span>

## <span data-ttu-id="50f77-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50f77-134">OUTPUTS</span></span>

### <span data-ttu-id="50f77-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="50f77-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="50f77-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50f77-136">NOTES</span></span>

## <span data-ttu-id="50f77-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50f77-137">RELATED LINKS</span></span>
