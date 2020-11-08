---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076612"
---
# <span data-ttu-id="7c140-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7c140-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="7c140-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c140-102">SYNOPSIS</span></span>


## <span data-ttu-id="7c140-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c140-103">SYNTAX</span></span>

### <span data-ttu-id="7c140-104">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c140-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c140-105">Получить</span><span class="sxs-lookup"><span data-stu-id="7c140-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7c140-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7c140-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7c140-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c140-107">DESCRIPTION</span></span>


## <span data-ttu-id="7c140-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c140-108">EXAMPLES</span></span>

### <span data-ttu-id="7c140-109">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="7c140-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="7c140-110">Получите список квот хранилища.</span><span class="sxs-lookup"><span data-stu-id="7c140-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="7c140-111">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="7c140-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="7c140-112">Получение сведений об указанной квоте хранилища по имени.</span><span class="sxs-lookup"><span data-stu-id="7c140-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="7c140-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c140-113">PARAMETERS</span></span>

### <span data-ttu-id="7c140-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c140-114">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c140-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c140-115">-InputObject</span></span>
<span data-ttu-id="7c140-116">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7c140-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7c140-117">-Location</span><span class="sxs-lookup"><span data-stu-id="7c140-117">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c140-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c140-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c140-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c140-119">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c140-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c140-120">CommonParameters</span></span>
<span data-ttu-id="7c140-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c140-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c140-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c140-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c140-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c140-123">INPUTS</span></span>

### <span data-ttu-id="7c140-124">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7c140-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="7c140-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c140-125">OUTPUTS</span></span>

### <span data-ttu-id="7c140-126">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="7c140-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="7c140-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c140-127">NOTES</span></span>

<span data-ttu-id="7c140-128">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7c140-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c140-129">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c140-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7c140-130">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="7c140-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="7c140-131">`[AccountId <String>]`: Внутренний идентификатор учетной записи хранения, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="7c140-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="7c140-132">`[AsyncOperationId <String>]`: Идентификатор асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="7c140-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="7c140-133">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="7c140-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c140-134">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="7c140-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="7c140-135">`[QuotaName <String>]`: Имя дисковой квоты.</span><span class="sxs-lookup"><span data-stu-id="7c140-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="7c140-136">`[ResourceGroup <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c140-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="7c140-137">`[ServiceName <String>]`: Имя службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="7c140-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="7c140-138">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="7c140-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="7c140-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c140-139">RELATED LINKS</span></span>

