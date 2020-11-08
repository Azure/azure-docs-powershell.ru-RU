---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076750"
---
# <span data-ttu-id="3184b-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="3184b-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="3184b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3184b-102">SYNOPSIS</span></span>


## <span data-ttu-id="3184b-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3184b-103">SYNTAX</span></span>

### <span data-ttu-id="3184b-104">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3184b-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3184b-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3184b-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3184b-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3184b-106">DESCRIPTION</span></span>


## <span data-ttu-id="3184b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3184b-107">EXAMPLES</span></span>

### <span data-ttu-id="3184b-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="3184b-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="3184b-109">Удалите квоту хранилища по имени.</span><span class="sxs-lookup"><span data-stu-id="3184b-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="3184b-110">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="3184b-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="3184b-111">Удалите квоту хранилища посредством конвейера.</span><span class="sxs-lookup"><span data-stu-id="3184b-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="3184b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3184b-112">PARAMETERS</span></span>

### <span data-ttu-id="3184b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3184b-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="3184b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3184b-114">-InputObject</span></span>
<span data-ttu-id="3184b-115">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3184b-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3184b-116">-Location</span><span class="sxs-lookup"><span data-stu-id="3184b-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3184b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3184b-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3184b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3184b-118">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3184b-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3184b-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3184b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3184b-120">-Confirm</span></span>
<span data-ttu-id="3184b-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3184b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3184b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3184b-122">-WhatIf</span></span>
<span data-ttu-id="3184b-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3184b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3184b-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3184b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3184b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3184b-125">CommonParameters</span></span>
<span data-ttu-id="3184b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3184b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3184b-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3184b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3184b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3184b-128">INPUTS</span></span>

### <span data-ttu-id="3184b-129">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3184b-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="3184b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3184b-130">OUTPUTS</span></span>

### <span data-ttu-id="3184b-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3184b-131">System.Boolean</span></span>



## <span data-ttu-id="3184b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3184b-132">NOTES</span></span>

<span data-ttu-id="3184b-133">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3184b-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3184b-134">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3184b-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3184b-135">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="3184b-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="3184b-136">`[AccountId <String>]`: Внутренний идентификатор учетной записи хранения, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="3184b-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="3184b-137">`[AsyncOperationId <String>]`: Идентификатор асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="3184b-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="3184b-138">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3184b-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3184b-139">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3184b-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="3184b-140">`[QuotaName <String>]`: Имя дисковой квоты.</span><span class="sxs-lookup"><span data-stu-id="3184b-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="3184b-141">`[ResourceGroup <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3184b-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="3184b-142">`[ServiceName <String>]`: Имя службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="3184b-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="3184b-143">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="3184b-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="3184b-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3184b-144">RELATED LINKS</span></span>
