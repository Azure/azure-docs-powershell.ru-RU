---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247802"
---
# <span data-ttu-id="16cd6-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="16cd6-101">Get-AzImportExport</span></span>

## <span data-ttu-id="16cd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16cd6-102">SYNOPSIS</span></span>
<span data-ttu-id="16cd6-103">Получает сведения о существующем задании.</span><span class="sxs-lookup"><span data-stu-id="16cd6-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="16cd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16cd6-104">SYNTAX</span></span>

### <span data-ttu-id="16cd6-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16cd6-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16cd6-106">Получить</span><span class="sxs-lookup"><span data-stu-id="16cd6-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16cd6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="16cd6-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16cd6-108">List1</span><span class="sxs-lookup"><span data-stu-id="16cd6-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="16cd6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16cd6-109">DESCRIPTION</span></span>
<span data-ttu-id="16cd6-110">Получает сведения о существующем задании.</span><span class="sxs-lookup"><span data-stu-id="16cd6-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="16cd6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16cd6-111">EXAMPLES</span></span>

### <span data-ttu-id="16cd6-112">Пример 1: получение задания ImportExport с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="16cd6-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="16cd6-113">Этот командлет получает задание ImportExport с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16cd6-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="16cd6-114">Пример 2: получение ImportExport задания по группе ресурсов и названию задания</span><span class="sxs-lookup"><span data-stu-id="16cd6-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="16cd6-115">Этот командлет получает ImportExport задание по группе ресурсов и имени задания.</span><span class="sxs-lookup"><span data-stu-id="16cd6-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="16cd6-116">Пример 3: список всех заданий ImportExport в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="16cd6-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="16cd6-117">Этот командлет выводит список всех заданий ImportExport в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16cd6-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="16cd6-118">Пример 4: получение ImportExport задания по удостоверению</span><span class="sxs-lookup"><span data-stu-id="16cd6-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="16cd6-119">Этот командлет возвращает ImportExport задание по идентификационному списку.</span><span class="sxs-lookup"><span data-stu-id="16cd6-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="16cd6-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16cd6-120">PARAMETERS</span></span>

### <span data-ttu-id="16cd6-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="16cd6-121">-AcceptLanguage</span></span>
<span data-ttu-id="16cd6-122">Указывает предпочтительный язык ответа.</span><span class="sxs-lookup"><span data-stu-id="16cd6-122">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cd6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16cd6-123">-DefaultProfile</span></span>
<span data-ttu-id="16cd6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16cd6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16cd6-125">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="16cd6-125">-Filter</span></span>
<span data-ttu-id="16cd6-126">Может использоваться для ограничения результатов определенными условиями.</span><span class="sxs-lookup"><span data-stu-id="16cd6-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cd6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16cd6-127">-InputObject</span></span>
<span data-ttu-id="16cd6-128">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="16cd6-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16cd6-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16cd6-129">-Name</span></span>
<span data-ttu-id="16cd6-130">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="16cd6-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cd6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16cd6-131">-ResourceGroupName</span></span>
<span data-ttu-id="16cd6-132">Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="16cd6-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cd6-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16cd6-133">-SubscriptionId</span></span>
<span data-ttu-id="16cd6-134">Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="16cd6-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cd6-135">-Top</span><span class="sxs-lookup"><span data-stu-id="16cd6-135">-Top</span></span>
<span data-ttu-id="16cd6-136">Целое число, которое указывает, сколько заданий в большинстве должно быть возвращено.</span><span class="sxs-lookup"><span data-stu-id="16cd6-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="16cd6-137">Значение не может превышать 100.</span><span class="sxs-lookup"><span data-stu-id="16cd6-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16cd6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16cd6-138">CommonParameters</span></span>
<span data-ttu-id="16cd6-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16cd6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16cd6-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16cd6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16cd6-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16cd6-141">INPUTS</span></span>

### <span data-ttu-id="16cd6-142">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="16cd6-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="16cd6-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16cd6-143">OUTPUTS</span></span>

### <span data-ttu-id="16cd6-144">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="16cd6-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="16cd6-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="16cd6-145">NOTES</span></span>

<span data-ttu-id="16cd6-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="16cd6-146">ALIASES</span></span>

<span data-ttu-id="16cd6-147">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="16cd6-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16cd6-148">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="16cd6-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16cd6-149">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16cd6-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16cd6-150">INPUTOBJECT <IImportExportIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="16cd6-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16cd6-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="16cd6-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16cd6-152">`[JobName <String>]`: Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="16cd6-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="16cd6-153">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="16cd6-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="16cd6-154">Например, "Западная США" или "westus".</span><span class="sxs-lookup"><span data-stu-id="16cd6-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="16cd6-155">`[ResourceGroupName <String>]`: Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="16cd6-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="16cd6-156">`[SubscriptionId <String>]`: Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="16cd6-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="16cd6-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16cd6-157">RELATED LINKS</span></span>

