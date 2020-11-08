---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077041"
---
# <span data-ttu-id="378b3-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="378b3-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="378b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="378b3-102">SYNOPSIS</span></span>
<span data-ttu-id="378b3-103">Возвращает указанное расположение резервной копии на основе имени.</span><span class="sxs-lookup"><span data-stu-id="378b3-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="378b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="378b3-104">SYNTAX</span></span>

### <span data-ttu-id="378b3-105">Get (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="378b3-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="378b3-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="378b3-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="378b3-107">Список</span><span class="sxs-lookup"><span data-stu-id="378b3-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="378b3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="378b3-108">DESCRIPTION</span></span>
<span data-ttu-id="378b3-109">Возвращает указанное расположение резервной копии на основе имени.</span><span class="sxs-lookup"><span data-stu-id="378b3-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="378b3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="378b3-110">EXAMPLES</span></span>

### <span data-ttu-id="378b3-111">Пример 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="378b3-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="378b3-112">Скачайте конфигурацию стека для резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="378b3-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="378b3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="378b3-113">PARAMETERS</span></span>

### <span data-ttu-id="378b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378b3-114">-DefaultProfile</span></span>
<span data-ttu-id="378b3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="378b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="378b3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="378b3-116">-InputObject</span></span>
<span data-ttu-id="378b3-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="378b3-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="378b3-118">-Location</span><span class="sxs-lookup"><span data-stu-id="378b3-118">-Location</span></span>
<span data-ttu-id="378b3-119">Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="378b3-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="378b3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="378b3-120">-ResourceGroupName</span></span>
<span data-ttu-id="378b3-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="378b3-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="378b3-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="378b3-122">-Skip</span></span>
<span data-ttu-id="378b3-123">Параметр пропуска OData.</span><span class="sxs-lookup"><span data-stu-id="378b3-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="378b3-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="378b3-124">-SubscriptionId</span></span>
<span data-ttu-id="378b3-125">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="378b3-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="378b3-126">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="378b3-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="378b3-127">-Top</span><span class="sxs-lookup"><span data-stu-id="378b3-127">-Top</span></span>
<span data-ttu-id="378b3-128">Параметр TOP для OData.</span><span class="sxs-lookup"><span data-stu-id="378b3-128">OData top parameter.</span></span>

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

### <span data-ttu-id="378b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378b3-129">CommonParameters</span></span>
<span data-ttu-id="378b3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="378b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378b3-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="378b3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378b3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="378b3-132">INPUTS</span></span>

### <span data-ttu-id="378b3-133">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="378b3-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="378b3-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="378b3-134">OUTPUTS</span></span>

### <span data-ttu-id="378b3-135">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="378b3-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="378b3-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="378b3-136">NOTES</span></span>

<span data-ttu-id="378b3-137">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="378b3-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="378b3-138">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="378b3-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="378b3-139">INPUTOBJECT <IBackupAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="378b3-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="378b3-140">`[Backup <String>]`: Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="378b3-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="378b3-141">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="378b3-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="378b3-142">`[Location <String>]`: Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="378b3-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="378b3-143">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="378b3-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="378b3-144">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="378b3-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="378b3-145">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="378b3-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="378b3-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="378b3-146">RELATED LINKS</span></span>
