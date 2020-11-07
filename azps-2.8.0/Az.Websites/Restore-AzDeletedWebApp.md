---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a413c0b021a167252469f211b5a8e5af670f9ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907157"
---
# <span data-ttu-id="3422f-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3422f-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="3422f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3422f-102">SYNOPSIS</span></span>
<span data-ttu-id="3422f-103">Восстанавливает удаленное веб-приложение в новом или существующем веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="3422f-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="3422f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3422f-104">SYNTAX</span></span>

### <span data-ttu-id="3422f-105">FromDeletedResourceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3422f-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3422f-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="3422f-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3422f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3422f-107">DESCRIPTION</span></span>
<span data-ttu-id="3422f-108">Командлет **RESTORE-AzDeletedWebApp** восстанавливает удаленное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="3422f-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="3422f-109">Веб-приложение, указанное в TargetResourceGroupName, TargetName и TargetSlot, будет заменено содержимым и параметрами удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="3422f-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="3422f-110">Если целевые параметры не заданы, они будут автоматически заполнены группой ресурсов, именем и областью удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="3422f-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="3422f-111">Если целевое веб-приложение не существует, оно будет автоматически создано в плане служб приложений, заданном в TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="3422f-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="3422f-112">Параметр ключа RestoreContentOnly можно использовать для восстановления только удаленных файлов приложения без параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="3422f-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="3422f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3422f-113">EXAMPLES</span></span>

### <span data-ttu-id="3422f-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3422f-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="3422f-115">Восстанавливает удаленное приложение с именем ContosoApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="3422f-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="3422f-116">Новое приложение с тем же именем и группой ресурсов будет создано в плане служб приложений с именем ContosoPlan, и в него будут восстановлены файлы и параметры удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="3422f-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="3422f-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3422f-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="3422f-118">Восстанавливает промежуточный слот для удаленного приложения с именем ContosoApp, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="3422f-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="3422f-119">Веб-приложение ContosoRestore, которое принадлежит к группе ресурсов Default-Web-EastUS, будет переписано.</span><span class="sxs-lookup"><span data-stu-id="3422f-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="3422f-120">Удаленные параметры веб-приложения не будут восстановлены.</span><span class="sxs-lookup"><span data-stu-id="3422f-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="3422f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3422f-121">PARAMETERS</span></span>

### <span data-ttu-id="3422f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3422f-122">-AsJob</span></span>
<span data-ttu-id="3422f-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3422f-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3422f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3422f-124">-DefaultProfile</span></span>
<span data-ttu-id="3422f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3422f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3422f-126">-Force</span></span>
<span data-ttu-id="3422f-127">Выполнение восстановления без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3422f-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3422f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3422f-128">-InputObject</span></span>
<span data-ttu-id="3422f-129">Удаленное веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-129">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3422f-130">-Location</span><span class="sxs-lookup"><span data-stu-id="3422f-130">-Location</span></span>
<span data-ttu-id="3422f-131">Расположение удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-131">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3422f-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3422f-132">-Name</span></span>
<span data-ttu-id="3422f-133">Имя удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-133">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3422f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3422f-134">-ResourceGroupName</span></span>
<span data-ttu-id="3422f-135">Группа ресурсов удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-135">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3422f-136">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="3422f-136">-RestoreContentOnly</span></span>
<span data-ttu-id="3422f-137">Восстановите файлы веб-приложения, но не восстанавливайте параметры.</span><span class="sxs-lookup"><span data-stu-id="3422f-137">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="3422f-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="3422f-138">-Slot</span></span>
<span data-ttu-id="3422f-139">Удаленная область веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-139">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3422f-140">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="3422f-140">-TargetAppServicePlanName</span></span>
<span data-ttu-id="3422f-141">План служб приложений для нового веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-141">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="3422f-142">-TargetName</span><span class="sxs-lookup"><span data-stu-id="3422f-142">-TargetName</span></span>
<span data-ttu-id="3422f-143">Имя нового веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-143">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="3422f-144">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3422f-144">-TargetResourceGroupName</span></span>
<span data-ttu-id="3422f-145">Группа ресурсов, содержащая новое веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-145">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="3422f-146">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="3422f-146">-TargetSlot</span></span>
<span data-ttu-id="3422f-147">Имя новой области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3422f-147">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="3422f-148">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="3422f-148">-UseDisasterRecovery</span></span>
<span data-ttu-id="3422f-149">Используйте для восстановления удаленного приложения из неподключенного устройства масштабирования.</span><span class="sxs-lookup"><span data-stu-id="3422f-149">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="3422f-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3422f-150">-Confirm</span></span>
<span data-ttu-id="3422f-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3422f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3422f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3422f-152">-WhatIf</span></span>
<span data-ttu-id="3422f-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3422f-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3422f-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3422f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3422f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3422f-155">CommonParameters</span></span>
<span data-ttu-id="3422f-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3422f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3422f-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3422f-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3422f-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3422f-158">INPUTS</span></span>

### <span data-ttu-id="3422f-159">Microsoft. Azure. Commands. Apps. командлеты. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3422f-159">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="3422f-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3422f-160">OUTPUTS</span></span>

### <span data-ttu-id="3422f-161">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="3422f-161">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3422f-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="3422f-162">NOTES</span></span>

## <span data-ttu-id="3422f-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3422f-163">RELATED LINKS</span></span>

[<span data-ttu-id="3422f-164">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3422f-164">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)