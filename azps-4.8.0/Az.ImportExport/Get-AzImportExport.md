---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242747"
---
# <span data-ttu-id="36151-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="36151-101">Get-AzImportExport</span></span>

## <span data-ttu-id="36151-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36151-102">SYNOPSIS</span></span>
<span data-ttu-id="36151-103">Получает сведения о существующем задании.</span><span class="sxs-lookup"><span data-stu-id="36151-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="36151-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36151-104">SYNTAX</span></span>

### <span data-ttu-id="36151-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36151-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36151-106">Получить</span><span class="sxs-lookup"><span data-stu-id="36151-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36151-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36151-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36151-108">List1</span><span class="sxs-lookup"><span data-stu-id="36151-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36151-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36151-109">DESCRIPTION</span></span>
<span data-ttu-id="36151-110">Получает сведения о существующем задании.</span><span class="sxs-lookup"><span data-stu-id="36151-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="36151-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36151-111">EXAMPLES</span></span>

### <span data-ttu-id="36151-112">Пример 1: получение задания ImportExport с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="36151-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="36151-113">Этот командлет получает задание ImportExport с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36151-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="36151-114">Пример 2: получение ImportExport задания по группе ресурсов и названию задания</span><span class="sxs-lookup"><span data-stu-id="36151-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="36151-115">Этот командлет получает ImportExport задание по группе ресурсов и имени задания.</span><span class="sxs-lookup"><span data-stu-id="36151-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="36151-116">Пример 3: список всех заданий ImportExport в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="36151-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="36151-117">Этот командлет выводит список всех заданий ImportExport в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="36151-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="36151-118">Пример 4: получение ImportExport задания по удостоверению</span><span class="sxs-lookup"><span data-stu-id="36151-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="36151-119">Этот командлет возвращает ImportExport задание по идентификационному списку.</span><span class="sxs-lookup"><span data-stu-id="36151-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="36151-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36151-120">PARAMETERS</span></span>

### <span data-ttu-id="36151-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="36151-121">-AcceptLanguage</span></span>
<span data-ttu-id="36151-122">Указывает предпочтительный язык ответа.</span><span class="sxs-lookup"><span data-stu-id="36151-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="36151-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36151-123">-DefaultProfile</span></span>
<span data-ttu-id="36151-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36151-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36151-125">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="36151-125">-Filter</span></span>
<span data-ttu-id="36151-126">Может использоваться для ограничения результатов определенными условиями.</span><span class="sxs-lookup"><span data-stu-id="36151-126">Can be used to restrict the results to certain conditions.</span></span>

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

### <span data-ttu-id="36151-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36151-127">-InputObject</span></span>
<span data-ttu-id="36151-128">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="36151-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36151-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36151-129">-Name</span></span>
<span data-ttu-id="36151-130">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="36151-130">The name of the import/export job.</span></span>

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

### <span data-ttu-id="36151-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36151-131">-ResourceGroupName</span></span>
<span data-ttu-id="36151-132">Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="36151-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="36151-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36151-133">-SubscriptionId</span></span>
<span data-ttu-id="36151-134">Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="36151-134">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="36151-135">-Top</span><span class="sxs-lookup"><span data-stu-id="36151-135">-Top</span></span>
<span data-ttu-id="36151-136">Целое число, которое указывает, сколько заданий в большинстве должно быть возвращено.</span><span class="sxs-lookup"><span data-stu-id="36151-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="36151-137">Значение не может превышать 100.</span><span class="sxs-lookup"><span data-stu-id="36151-137">The value cannot exceed 100.</span></span>

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

### <span data-ttu-id="36151-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36151-138">CommonParameters</span></span>
<span data-ttu-id="36151-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36151-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36151-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36151-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36151-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36151-141">INPUTS</span></span>

### <span data-ttu-id="36151-142">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="36151-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="36151-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36151-143">OUTPUTS</span></span>

### <span data-ttu-id="36151-144">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="36151-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="36151-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="36151-145">NOTES</span></span>

<span data-ttu-id="36151-146">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="36151-146">ALIASES</span></span>

<span data-ttu-id="36151-147">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="36151-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36151-148">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="36151-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36151-149">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="36151-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36151-150">INPUTOBJECT <IImportExportIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="36151-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36151-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="36151-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36151-152">`[JobName <String>]`: Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="36151-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="36151-153">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="36151-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="36151-154">Например, "Западная США" или "westus".</span><span class="sxs-lookup"><span data-stu-id="36151-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="36151-155">`[ResourceGroupName <String>]`: Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="36151-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="36151-156">`[SubscriptionId <String>]`: Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="36151-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="36151-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36151-157">RELATED LINKS</span></span>

