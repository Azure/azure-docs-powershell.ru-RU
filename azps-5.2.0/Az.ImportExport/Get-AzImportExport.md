---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397119"
---
# <span data-ttu-id="11599-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="11599-101">Get-AzImportExport</span></span>

## <span data-ttu-id="11599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11599-102">SYNOPSIS</span></span>
<span data-ttu-id="11599-103">Получает сведения о существующем задание.</span><span class="sxs-lookup"><span data-stu-id="11599-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="11599-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11599-104">SYNTAX</span></span>

### <span data-ttu-id="11599-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11599-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11599-106">Получить</span><span class="sxs-lookup"><span data-stu-id="11599-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11599-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="11599-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="11599-108">Список1</span><span class="sxs-lookup"><span data-stu-id="11599-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="11599-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11599-109">DESCRIPTION</span></span>
<span data-ttu-id="11599-110">Получает сведения о существующем задание.</span><span class="sxs-lookup"><span data-stu-id="11599-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="11599-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11599-111">EXAMPLES</span></span>

### <span data-ttu-id="11599-112">Пример 1. Получить задание ImportExport с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="11599-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="11599-113">Этот cmdlet получает задание ImportExport с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="11599-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="11599-114">Пример 2. Получить задание ImportExport по группе ресурсов и имени задания</span><span class="sxs-lookup"><span data-stu-id="11599-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="11599-115">Этот cmdlet получает задание ImportExport по группе ресурсов и имени задания.</span><span class="sxs-lookup"><span data-stu-id="11599-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="11599-116">Пример 3. Список всех заданий ImportExport в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="11599-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="11599-117">Этот cmdlet lists all the ImportExport jobs in specified resource group.</span><span class="sxs-lookup"><span data-stu-id="11599-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="11599-118">Пример 4. Получить задание ImportExport по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="11599-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="11599-119">Этот список получает задание ImportExport по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="11599-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="11599-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11599-120">PARAMETERS</span></span>

### <span data-ttu-id="11599-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="11599-121">-AcceptLanguage</span></span>
<span data-ttu-id="11599-122">Указывает предпочтительный язык для ответа.</span><span class="sxs-lookup"><span data-stu-id="11599-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="11599-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11599-123">-DefaultProfile</span></span>
<span data-ttu-id="11599-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11599-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11599-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="11599-125">-Filter</span></span>
<span data-ttu-id="11599-126">Может использоваться для ограничения результатов определенными условиями.</span><span class="sxs-lookup"><span data-stu-id="11599-126">Can be used to restrict the results to certain conditions.</span></span>

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

### <span data-ttu-id="11599-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11599-127">-InputObject</span></span>
<span data-ttu-id="11599-128">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="11599-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="11599-129">-Name</span><span class="sxs-lookup"><span data-stu-id="11599-129">-Name</span></span>
<span data-ttu-id="11599-130">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="11599-130">The name of the import/export job.</span></span>

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

### <span data-ttu-id="11599-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11599-131">-ResourceGroupName</span></span>
<span data-ttu-id="11599-132">Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="11599-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="11599-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11599-133">-SubscriptionId</span></span>
<span data-ttu-id="11599-134">ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="11599-134">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="11599-135">-Top</span><span class="sxs-lookup"><span data-stu-id="11599-135">-Top</span></span>
<span data-ttu-id="11599-136">Значение, которое указывает, сколько должно быть возвращено заданий.</span><span class="sxs-lookup"><span data-stu-id="11599-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="11599-137">Значение не может превышать 100.</span><span class="sxs-lookup"><span data-stu-id="11599-137">The value cannot exceed 100.</span></span>

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

### <span data-ttu-id="11599-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11599-138">CommonParameters</span></span>
<span data-ttu-id="11599-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11599-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11599-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11599-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11599-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11599-141">INPUTS</span></span>

### <span data-ttu-id="11599-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="11599-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="11599-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11599-143">OUTPUTS</span></span>

### <span data-ttu-id="11599-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="11599-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="11599-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11599-145">NOTES</span></span>

<span data-ttu-id="11599-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="11599-146">ALIASES</span></span>

<span data-ttu-id="11599-147">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="11599-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11599-148">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="11599-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11599-149">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11599-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11599-150">INPUTOBJECT <IImportExportIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="11599-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="11599-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="11599-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="11599-152">`[JobName <String>]`: имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="11599-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="11599-153">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="11599-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="11599-154">Например, "Запад США" или "запад".</span><span class="sxs-lookup"><span data-stu-id="11599-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="11599-155">`[ResourceGroupName <String>]`. Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="11599-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="11599-156">`[SubscriptionId <String>]`: ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="11599-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="11599-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11599-157">RELATED LINKS</span></span>
