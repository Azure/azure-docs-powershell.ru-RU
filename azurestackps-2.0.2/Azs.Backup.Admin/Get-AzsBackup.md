---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077134"
---
# <span data-ttu-id="f859b-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="f859b-101">Get-AzsBackup</span></span>

## <span data-ttu-id="f859b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f859b-102">SYNOPSIS</span></span>
<span data-ttu-id="f859b-103">Возвращает резервное копирование из расположения на основе имени.</span><span class="sxs-lookup"><span data-stu-id="f859b-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="f859b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f859b-104">SYNTAX</span></span>

### <span data-ttu-id="f859b-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f859b-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f859b-106">Получить</span><span class="sxs-lookup"><span data-stu-id="f859b-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f859b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f859b-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f859b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f859b-108">DESCRIPTION</span></span>
<span data-ttu-id="f859b-109">Возвращает резервное копирование из расположения на основе имени.</span><span class="sxs-lookup"><span data-stu-id="f859b-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="f859b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f859b-110">EXAMPLES</span></span>

### <span data-ttu-id="f859b-111">Пример 1: создание резервных копий списка</span><span class="sxs-lookup"><span data-stu-id="f859b-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="f859b-112">Получение сведений sbout всех резервных копий стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="f859b-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="f859b-113">Пример 2: получение конкретной резервной копии</span><span class="sxs-lookup"><span data-stu-id="f859b-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="f859b-114">Получение сведений для указанной резервной копии стека Azure.</span><span class="sxs-lookup"><span data-stu-id="f859b-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="f859b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f859b-115">PARAMETERS</span></span>

### <span data-ttu-id="f859b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f859b-116">-DefaultProfile</span></span>
<span data-ttu-id="f859b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f859b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f859b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f859b-118">-InputObject</span></span>
<span data-ttu-id="f859b-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="f859b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f859b-120">-Location</span><span class="sxs-lookup"><span data-stu-id="f859b-120">-Location</span></span>
<span data-ttu-id="f859b-121">Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f859b-121">Name of the backup location.</span></span>

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

### <span data-ttu-id="f859b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f859b-122">-Name</span></span>
<span data-ttu-id="f859b-123">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f859b-123">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f859b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f859b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f859b-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f859b-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f859b-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="f859b-126">-Skip</span></span>
<span data-ttu-id="f859b-127">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="f859b-127">OData skip parameter.</span></span>

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

### <span data-ttu-id="f859b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f859b-128">-SubscriptionId</span></span>
<span data-ttu-id="f859b-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f859b-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f859b-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f859b-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f859b-131">-Top</span><span class="sxs-lookup"><span data-stu-id="f859b-131">-Top</span></span>
<span data-ttu-id="f859b-132">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="f859b-132">OData top parameter.</span></span>

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

### <span data-ttu-id="f859b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f859b-133">CommonParameters</span></span>
<span data-ttu-id="f859b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f859b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f859b-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f859b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f859b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f859b-136">INPUTS</span></span>

### <span data-ttu-id="f859b-137">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f859b-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="f859b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f859b-138">OUTPUTS</span></span>

### <span data-ttu-id="f859b-139">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. Api20180901. IBackup</span><span class="sxs-lookup"><span data-stu-id="f859b-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="f859b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="f859b-140">NOTES</span></span>

<span data-ttu-id="f859b-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f859b-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f859b-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f859b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f859b-143">INPUTOBJECT <IBackupAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="f859b-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f859b-144">`[Backup <String>]`: Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f859b-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="f859b-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="f859b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f859b-146">`[Location <String>]`: Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="f859b-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="f859b-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f859b-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f859b-148">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f859b-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f859b-149">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="f859b-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f859b-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f859b-150">RELATED LINKS</span></span>

