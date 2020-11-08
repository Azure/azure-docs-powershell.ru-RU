---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/start-azsbackup
schema: 2.0.0
ms.openlocfilehash: 37fc3ddb1c878bc8b6b1e14d920a5747edce0cd3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075350"
---
# <span data-ttu-id="e5c10-101">Start-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="e5c10-101">Start-AzsBackup</span></span>

## <span data-ttu-id="e5c10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5c10-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c10-103">Создание резервной копии определенного местоположения.</span><span class="sxs-lookup"><span data-stu-id="e5c10-103">Back up a specific location.</span></span>

## <span data-ttu-id="e5c10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5c10-104">SYNTAX</span></span>

### <span data-ttu-id="e5c10-105">Создать (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5c10-105">Create (Default)</span></span>
```
Start-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e5c10-106">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e5c10-106">CreateViaIdentity</span></span>
```
Start-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e5c10-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c10-107">DESCRIPTION</span></span>
<span data-ttu-id="e5c10-108">Создание резервной копии определенного местоположения.</span><span class="sxs-lookup"><span data-stu-id="e5c10-108">Back up a specific location.</span></span>

## <span data-ttu-id="e5c10-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5c10-109">EXAMPLES</span></span>

### <span data-ttu-id="e5c10-110">Пример 1: запуск azurestack резервного копирования</span><span class="sxs-lookup"><span data-stu-id="e5c10-110">Example 1: Start azurestack backup</span></span>
```powershell
PS C:\>Start-AzsBackup

```

<span data-ttu-id="e5c10-111">Начните создавать резервные копии стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c10-111">Start an Azure Stack backup.</span></span>

## <span data-ttu-id="e5c10-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5c10-112">PARAMETERS</span></span>

### <span data-ttu-id="e5c10-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5c10-113">-AsJob</span></span>
<span data-ttu-id="e5c10-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e5c10-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e5c10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c10-115">-DefaultProfile</span></span>
<span data-ttu-id="e5c10-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c10-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c10-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5c10-117">-InputObject</span></span>
<span data-ttu-id="e5c10-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e5c10-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e5c10-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e5c10-119">-Location</span></span>
<span data-ttu-id="e5c10-120">Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e5c10-120">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e5c10-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="e5c10-121">-NoWait</span></span>
<span data-ttu-id="e5c10-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="e5c10-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e5c10-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c10-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5c10-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5c10-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e5c10-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5c10-125">-SubscriptionId</span></span>
<span data-ttu-id="e5c10-126">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c10-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e5c10-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e5c10-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e5c10-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5c10-128">-Confirm</span></span>
<span data-ttu-id="e5c10-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5c10-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5c10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5c10-130">-WhatIf</span></span>
<span data-ttu-id="e5c10-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5c10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5c10-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5c10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5c10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c10-133">CommonParameters</span></span>
<span data-ttu-id="e5c10-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5c10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c10-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5c10-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c10-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5c10-136">INPUTS</span></span>

### <span data-ttu-id="e5c10-137">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e5c10-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="e5c10-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c10-138">OUTPUTS</span></span>

### <span data-ttu-id="e5c10-139">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="e5c10-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="e5c10-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5c10-140">NOTES</span></span>

<span data-ttu-id="e5c10-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e5c10-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5c10-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5c10-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e5c10-143">INPUTOBJECT <IBackupAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e5c10-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5c10-144">`[Backup <String>]`: Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e5c10-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="e5c10-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e5c10-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5c10-146">`[Location <String>]`: Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="e5c10-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="e5c10-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5c10-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e5c10-148">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c10-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e5c10-149">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e5c10-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e5c10-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5c10-150">RELATED LINKS</span></span>

