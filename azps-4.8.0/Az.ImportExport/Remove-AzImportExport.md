---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236685"
---
# <span data-ttu-id="1134c-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="1134c-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="1134c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1134c-102">SYNOPSIS</span></span>
<span data-ttu-id="1134c-103">Удаление существующего задания.</span><span class="sxs-lookup"><span data-stu-id="1134c-103">Deletes an existing job.</span></span>
<span data-ttu-id="1134c-104">Удалять можно только задания в состоянии "создать" или "завершено".</span><span class="sxs-lookup"><span data-stu-id="1134c-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="1134c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1134c-105">SYNTAX</span></span>

### <span data-ttu-id="1134c-106">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1134c-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1134c-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1134c-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1134c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1134c-108">DESCRIPTION</span></span>
<span data-ttu-id="1134c-109">Удаление существующего задания.</span><span class="sxs-lookup"><span data-stu-id="1134c-109">Deletes an existing job.</span></span>
<span data-ttu-id="1134c-110">Удалять можно только задания в состоянии "создать" или "завершено".</span><span class="sxs-lookup"><span data-stu-id="1134c-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="1134c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1134c-111">EXAMPLES</span></span>

### <span data-ttu-id="1134c-112">Пример 1: удаление задания ImportExport по группе resourceGroup и имени сервера</span><span class="sxs-lookup"><span data-stu-id="1134c-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="1134c-113">Этот командлет удаляет задание ImportExport с помощью resourceGroup и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="1134c-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="1134c-114">Пример 2: удаление задания ImportExport по удостоверению</span><span class="sxs-lookup"><span data-stu-id="1134c-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="1134c-115">Эти командлеты удаляют задание ImportExport по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="1134c-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="1134c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1134c-116">PARAMETERS</span></span>

### <span data-ttu-id="1134c-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="1134c-117">-AcceptLanguage</span></span>
<span data-ttu-id="1134c-118">Указывает предпочтительный язык ответа.</span><span class="sxs-lookup"><span data-stu-id="1134c-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="1134c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1134c-119">-DefaultProfile</span></span>
<span data-ttu-id="1134c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1134c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1134c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1134c-121">-InputObject</span></span>
<span data-ttu-id="1134c-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1134c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1134c-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1134c-123">-Name</span></span>
<span data-ttu-id="1134c-124">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="1134c-124">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1134c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1134c-125">-PassThru</span></span>
<span data-ttu-id="1134c-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1134c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1134c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1134c-127">-ResourceGroupName</span></span>
<span data-ttu-id="1134c-128">Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="1134c-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1134c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1134c-129">-SubscriptionId</span></span>
<span data-ttu-id="1134c-130">Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="1134c-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="1134c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1134c-131">-Confirm</span></span>
<span data-ttu-id="1134c-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1134c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1134c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1134c-133">-WhatIf</span></span>
<span data-ttu-id="1134c-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1134c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1134c-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1134c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1134c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1134c-136">CommonParameters</span></span>
<span data-ttu-id="1134c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1134c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1134c-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1134c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1134c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1134c-139">INPUTS</span></span>

### <span data-ttu-id="1134c-140">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="1134c-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="1134c-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1134c-141">OUTPUTS</span></span>

### <span data-ttu-id="1134c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1134c-142">System.Boolean</span></span>

## <span data-ttu-id="1134c-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="1134c-143">NOTES</span></span>

<span data-ttu-id="1134c-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="1134c-144">ALIASES</span></span>

<span data-ttu-id="1134c-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1134c-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1134c-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1134c-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1134c-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1134c-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1134c-148">INPUTOBJECT <IImportExportIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="1134c-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1134c-149">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="1134c-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1134c-150">`[JobName <String>]`: Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="1134c-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="1134c-151">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="1134c-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="1134c-152">Например, "Западная США" или "westus".</span><span class="sxs-lookup"><span data-stu-id="1134c-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="1134c-153">`[ResourceGroupName <String>]`: Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="1134c-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="1134c-154">`[SubscriptionId <String>]`: Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="1134c-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="1134c-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1134c-155">RELATED LINKS</span></span>
