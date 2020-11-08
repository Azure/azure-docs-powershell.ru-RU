---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075168"
---
# <span data-ttu-id="be6d8-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="be6d8-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="be6d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be6d8-102">SYNOPSIS</span></span>


## <span data-ttu-id="be6d8-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be6d8-103">SYNTAX</span></span>

### <span data-ttu-id="be6d8-104">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be6d8-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="be6d8-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="be6d8-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be6d8-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be6d8-106">DESCRIPTION</span></span>


## <span data-ttu-id="be6d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be6d8-107">EXAMPLES</span></span>

### <span data-ttu-id="be6d8-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="be6d8-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="be6d8-109">Удалите квоту хранилища по имени.</span><span class="sxs-lookup"><span data-stu-id="be6d8-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="be6d8-110">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="be6d8-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="be6d8-111">Удалите квоту хранилища посредством конвейера.</span><span class="sxs-lookup"><span data-stu-id="be6d8-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="be6d8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be6d8-112">PARAMETERS</span></span>

### <span data-ttu-id="be6d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be6d8-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="be6d8-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be6d8-114">-InputObject</span></span>
<span data-ttu-id="be6d8-115">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="be6d8-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="be6d8-116">-Location</span><span class="sxs-lookup"><span data-stu-id="be6d8-116">-Location</span></span>


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

### <span data-ttu-id="be6d8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be6d8-117">-Name</span></span>


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

### <span data-ttu-id="be6d8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be6d8-118">-PassThru</span></span>


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

### <span data-ttu-id="be6d8-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be6d8-119">-SubscriptionId</span></span>


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

### <span data-ttu-id="be6d8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be6d8-120">-Confirm</span></span>
<span data-ttu-id="be6d8-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be6d8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be6d8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be6d8-122">-WhatIf</span></span>
<span data-ttu-id="be6d8-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be6d8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be6d8-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be6d8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be6d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be6d8-125">CommonParameters</span></span>
<span data-ttu-id="be6d8-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be6d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be6d8-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be6d8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be6d8-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be6d8-128">INPUTS</span></span>

### <span data-ttu-id="be6d8-129">Microsoft. Azure. PowerShell. командлеты. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="be6d8-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="be6d8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be6d8-130">OUTPUTS</span></span>

### <span data-ttu-id="be6d8-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be6d8-131">System.Boolean</span></span>



## <span data-ttu-id="be6d8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="be6d8-132">NOTES</span></span>

<span data-ttu-id="be6d8-133">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be6d8-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be6d8-134">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be6d8-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="be6d8-135">INPUTOBJECT <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="be6d8-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="be6d8-136">`[AccountId <String>]`: Внутренний идентификатор учетной записи хранения, невидимый для клиента.</span><span class="sxs-lookup"><span data-stu-id="be6d8-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="be6d8-137">`[AsyncOperationId <String>]`: Идентификатор асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="be6d8-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="be6d8-138">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="be6d8-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be6d8-139">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="be6d8-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="be6d8-140">`[QuotaName <String>]`: Имя дисковой квоты.</span><span class="sxs-lookup"><span data-stu-id="be6d8-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="be6d8-141">`[ResourceGroup <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be6d8-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="be6d8-142">`[ServiceName <String>]`: Имя службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="be6d8-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="be6d8-143">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="be6d8-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="be6d8-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be6d8-144">RELATED LINKS</span></span>

