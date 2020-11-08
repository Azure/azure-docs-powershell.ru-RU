---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: fb36cb0d1be46abb66a1c0cc97165f8eb9cc3913
ms.sourcegitcommit: f7edd4f5c4bebedc139cb01438081edc6ed560bd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/29/2020
ms.locfileid: "94077349"
---
# <span data-ttu-id="942a7-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="942a7-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="942a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="942a7-102">SYNOPSIS</span></span>
<span data-ttu-id="942a7-103">Получение экземпляра прогона обновления с использованием идентификатора.</span><span class="sxs-lookup"><span data-stu-id="942a7-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="942a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="942a7-104">SYNTAX</span></span>

### <span data-ttu-id="942a7-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="942a7-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="942a7-106">Получить</span><span class="sxs-lookup"><span data-stu-id="942a7-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="942a7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="942a7-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="942a7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="942a7-108">DESCRIPTION</span></span>
<span data-ttu-id="942a7-109">Получение экземпляра прогона обновления с использованием идентификатора.</span><span class="sxs-lookup"><span data-stu-id="942a7-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="942a7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="942a7-110">EXAMPLES</span></span>

### <span data-ttu-id="942a7-111">Пример 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="942a7-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="942a7-112">Если значение UpdateName не задано, Get-UpdateRun всегда будет запрашивать ввод.</span><span class="sxs-lookup"><span data-stu-id="942a7-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="942a7-113">После этого он будет выводить все экземпляры UpdateRun, которые завершились сбоем или успешно.</span><span class="sxs-lookup"><span data-stu-id="942a7-113">Once provided, it will output all instances of UpdateRun that were Failed or Successful</span></span>

### <span data-ttu-id="942a7-114">Пример 2: Get-AzsUpdateRun по UpdateName</span><span class="sxs-lookup"><span data-stu-id="942a7-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="942a7-115">Будут извлечены все UpdateRuns, связанные с определенным обновлением.</span><span class="sxs-lookup"><span data-stu-id="942a7-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="942a7-116">Пример 2: Get-AzsUpdateRun по имени</span><span class="sxs-lookup"><span data-stu-id="942a7-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="942a7-117">Будут извлечены все UpdateRuns, связанные с определенным обновлением и определенным именем.</span><span class="sxs-lookup"><span data-stu-id="942a7-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="942a7-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="942a7-118">PARAMETERS</span></span>

### <span data-ttu-id="942a7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942a7-119">-DefaultProfile</span></span>
<span data-ttu-id="942a7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="942a7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="942a7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="942a7-121">-InputObject</span></span>
<span data-ttu-id="942a7-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="942a7-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="942a7-123">-Location</span><span class="sxs-lookup"><span data-stu-id="942a7-123">-Location</span></span>
<span data-ttu-id="942a7-124">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="942a7-124">The name of the update location.</span></span>

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

### <span data-ttu-id="942a7-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="942a7-125">-Name</span></span>
<span data-ttu-id="942a7-126">Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="942a7-126">Update run identifier.</span></span>

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

### <span data-ttu-id="942a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="942a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="942a7-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="942a7-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="942a7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="942a7-129">-SubscriptionId</span></span>
<span data-ttu-id="942a7-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="942a7-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="942a7-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="942a7-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="942a7-132">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="942a7-132">-UpdateName</span></span>
<span data-ttu-id="942a7-133">Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="942a7-133">Name of the update.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="942a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942a7-134">CommonParameters</span></span>
<span data-ttu-id="942a7-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="942a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942a7-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="942a7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942a7-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="942a7-137">INPUTS</span></span>

### <span data-ttu-id="942a7-138">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="942a7-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="942a7-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="942a7-139">OUTPUTS</span></span>

### <span data-ttu-id="942a7-140">Microsoft. Azure. PowerShell. командлеты. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="942a7-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="942a7-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="942a7-141">NOTES</span></span>

<span data-ttu-id="942a7-142">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="942a7-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="942a7-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="942a7-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="942a7-144">INPUTOBJECT <IUpdateAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="942a7-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="942a7-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="942a7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="942a7-146">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="942a7-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="942a7-147">`[RunName <String>]`: Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="942a7-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="942a7-148">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="942a7-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="942a7-149">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="942a7-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="942a7-150">`[UpdateLocation <String>]`: Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="942a7-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="942a7-151">`[UpdateName <String>]`: Имя обновления.</span><span class="sxs-lookup"><span data-stu-id="942a7-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="942a7-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="942a7-152">RELATED LINKS</span></span>

