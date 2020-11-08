---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075327"
---
# <span data-ttu-id="220ff-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="220ff-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="220ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="220ff-102">SYNOPSIS</span></span>
<span data-ttu-id="220ff-103">Возвращает запрашиваемую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="220ff-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="220ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="220ff-104">SYNTAX</span></span>

### <span data-ttu-id="220ff-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="220ff-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="220ff-106">Получить</span><span class="sxs-lookup"><span data-stu-id="220ff-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="220ff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="220ff-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="220ff-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="220ff-108">DESCRIPTION</span></span>
<span data-ttu-id="220ff-109">Возвращает запрашиваемую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="220ff-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="220ff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="220ff-110">EXAMPLES</span></span>

### <span data-ttu-id="220ff-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="220ff-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="220ff-112">Получение списка учетных записей хранения (сводка).</span><span class="sxs-lookup"><span data-stu-id="220ff-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="220ff-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="220ff-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="220ff-114">Получите список учетных записей хранения с подробными сведениями и напечатайте состояние.</span><span class="sxs-lookup"><span data-stu-id="220ff-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="220ff-115">Пример 3:</span><span class="sxs-lookup"><span data-stu-id="220ff-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="220ff-116">Получение сведений об указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="220ff-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="220ff-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="220ff-117">PARAMETERS</span></span>

### <span data-ttu-id="220ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="220ff-118">-DefaultProfile</span></span>
<span data-ttu-id="220ff-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="220ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="220ff-120">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="220ff-120">-Filter</span></span>
<span data-ttu-id="220ff-121">Строка фильтра</span><span class="sxs-lookup"><span data-stu-id="220ff-121">Filter string</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="220ff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="220ff-122">-InputObject</span></span>
<span data-ttu-id="220ff-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="220ff-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="220ff-124">-Location</span><span class="sxs-lookup"><span data-stu-id="220ff-124">-Location</span></span>
<span data-ttu-id="220ff-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="220ff-125">Resource location.</span></span>

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

### <span data-ttu-id="220ff-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="220ff-126">-Name</span></span>
<span data-ttu-id="220ff-127">Внутренний идентификатор учетной записи хранилища, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="220ff-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="220ff-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="220ff-128">-SubscriptionId</span></span>
<span data-ttu-id="220ff-129">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="220ff-129">Subscription Id.</span></span>

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

### <span data-ttu-id="220ff-130">-Сводка</span><span class="sxs-lookup"><span data-stu-id="220ff-130">-Summary</span></span>
<span data-ttu-id="220ff-131">Выберите, следует ли вернуть сводную или подробную информацию.</span><span class="sxs-lookup"><span data-stu-id="220ff-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="220ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="220ff-132">CommonParameters</span></span>
<span data-ttu-id="220ff-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="220ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="220ff-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="220ff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="220ff-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="220ff-135">INPUTS</span></span>

### <span data-ttu-id="220ff-136">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="220ff-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="220ff-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="220ff-137">OUTPUTS</span></span>

### <span data-ttu-id="220ff-138">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. Api201908Preview. IStorageAccount</span><span class="sxs-lookup"><span data-stu-id="220ff-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="220ff-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="220ff-139">NOTES</span></span>

<span data-ttu-id="220ff-140">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="220ff-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="220ff-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="220ff-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="220ff-142">INPUTOBJECT <IStorageAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="220ff-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="220ff-143">`[AccountId <String>]`: Внутренний идентификатор учетной записи хранения, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="220ff-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="220ff-144">`[AsyncOperationId <String>]`: Идентификатор асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="220ff-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="220ff-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="220ff-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="220ff-146">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="220ff-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="220ff-147">`[QuotaName <String>]`: Имя дисковой квоты.</span><span class="sxs-lookup"><span data-stu-id="220ff-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="220ff-148">`[ResourceGroup <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="220ff-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="220ff-149">`[ServiceName <String>]`: Имя службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="220ff-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="220ff-150">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="220ff-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="220ff-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="220ff-151">RELATED LINKS</span></span>

