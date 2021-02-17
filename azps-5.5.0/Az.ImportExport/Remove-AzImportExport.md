---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/remove-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Remove-AzImportExport.md
ms.openlocfilehash: 0f78f68c9d5557b97366185b354823400eada97c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222361"
---
# <span data-ttu-id="4aa47-101">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="4aa47-101">Remove-AzImportExport</span></span>

## <span data-ttu-id="4aa47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aa47-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa47-103">Удаляет существующее задание.</span><span class="sxs-lookup"><span data-stu-id="4aa47-103">Deletes an existing job.</span></span>
<span data-ttu-id="4aa47-104">Удалять можно только задания в состояниях создания и завершения.</span><span class="sxs-lookup"><span data-stu-id="4aa47-104">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="4aa47-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4aa47-105">SYNTAX</span></span>

### <span data-ttu-id="4aa47-106">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4aa47-106">Delete (Default)</span></span>
```
Remove-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4aa47-107">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa47-107">DeleteViaIdentity</span></span>
```
Remove-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4aa47-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4aa47-108">DESCRIPTION</span></span>
<span data-ttu-id="4aa47-109">Удаляет существующее задание.</span><span class="sxs-lookup"><span data-stu-id="4aa47-109">Deletes an existing job.</span></span>
<span data-ttu-id="4aa47-110">Удалять можно только задания в состояниях создания и завершения.</span><span class="sxs-lookup"><span data-stu-id="4aa47-110">Only jobs in the Creating or Completed states can be deleted.</span></span>

## <span data-ttu-id="4aa47-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4aa47-111">EXAMPLES</span></span>

### <span data-ttu-id="4aa47-112">Пример 1. Удаление задания ImportExport по группам ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="4aa47-112">Example 1: Remove ImportExport job by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
```

<span data-ttu-id="4aa47-113">Этот cmdlet removes ImportExport job by resourceGroup and server name.</span><span class="sxs-lookup"><span data-stu-id="4aa47-113">This cmdlet removes ImportExport job by resourceGroup and server name.</span></span>

### <span data-ttu-id="4aa47-114">Пример 2. Удаление задания ImportExport по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="4aa47-114">Example 2: Remove ImportExport job by identity</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Remove-AzImportExport
 
```

<span data-ttu-id="4aa47-115">Этот cmdlet удаляет задание ImportExport по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="4aa47-115">These cmdlet removes ImportExport job by identity.</span></span>

## <span data-ttu-id="4aa47-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aa47-116">PARAMETERS</span></span>

### <span data-ttu-id="4aa47-117">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="4aa47-117">-AcceptLanguage</span></span>
<span data-ttu-id="4aa47-118">Указывает предпочтительный язык для ответа.</span><span class="sxs-lookup"><span data-stu-id="4aa47-118">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="4aa47-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa47-119">-DefaultProfile</span></span>
<span data-ttu-id="4aa47-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa47-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aa47-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aa47-121">-InputObject</span></span>
<span data-ttu-id="4aa47-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="4aa47-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4aa47-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4aa47-123">-Name</span></span>
<span data-ttu-id="4aa47-124">Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="4aa47-124">The name of the import/export job.</span></span>

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

### <span data-ttu-id="4aa47-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4aa47-125">-PassThru</span></span>
<span data-ttu-id="4aa47-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="4aa47-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4aa47-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa47-127">-ResourceGroupName</span></span>
<span data-ttu-id="4aa47-128">Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="4aa47-128">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="4aa47-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4aa47-129">-SubscriptionId</span></span>
<span data-ttu-id="4aa47-130">ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa47-130">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="4aa47-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aa47-131">-Confirm</span></span>
<span data-ttu-id="4aa47-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4aa47-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa47-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa47-133">-WhatIf</span></span>
<span data-ttu-id="4aa47-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4aa47-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa47-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4aa47-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa47-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa47-136">CommonParameters</span></span>
<span data-ttu-id="4aa47-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aa47-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa47-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aa47-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa47-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4aa47-139">INPUTS</span></span>

### <span data-ttu-id="4aa47-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="4aa47-140">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="4aa47-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4aa47-141">OUTPUTS</span></span>

### <span data-ttu-id="4aa47-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4aa47-142">System.Boolean</span></span>

## <span data-ttu-id="4aa47-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4aa47-143">NOTES</span></span>

<span data-ttu-id="4aa47-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4aa47-144">ALIASES</span></span>

<span data-ttu-id="4aa47-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4aa47-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4aa47-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4aa47-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4aa47-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4aa47-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4aa47-148">INPUTOBJECT <IImportExportIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="4aa47-148">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4aa47-149">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="4aa47-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4aa47-150">`[JobName <String>]`: имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="4aa47-150">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="4aa47-151">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="4aa47-151">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="4aa47-152">Например, "Запад США" или "запад".</span><span class="sxs-lookup"><span data-stu-id="4aa47-152">For example, West US or westus.</span></span>
  - <span data-ttu-id="4aa47-153">`[ResourceGroupName <String>]`. Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="4aa47-153">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="4aa47-154">`[SubscriptionId <String>]`: ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa47-154">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="4aa47-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4aa47-155">RELATED LINKS</span></span>

