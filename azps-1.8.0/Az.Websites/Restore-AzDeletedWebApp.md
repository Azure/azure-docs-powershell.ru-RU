---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a90a56417ab8b1b08d72cb9d00ebe7411a6f075c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728304"
---
# <span data-ttu-id="e1b9a-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e1b9a-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="e1b9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b9a-103">Восстанавливает удаленное веб-приложение в новом или существующем веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="e1b9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1b9a-104">SYNTAX</span></span>

### <span data-ttu-id="e1b9a-105">FromDeletedResourceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1b9a-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1b9a-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="e1b9a-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1b9a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1b9a-107">DESCRIPTION</span></span>
<span data-ttu-id="e1b9a-108">Командлет **RESTORE-AzDeletedWebApp** восстанавливает удаленное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="e1b9a-109">Веб-приложение, указанное в TargetResourceGroupName, TargetName и TargetSlot, будет заменено содержимым и параметрами удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="e1b9a-110">Если целевые параметры не заданы, они будут автоматически заполнены группой ресурсов, именем и областью удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="e1b9a-111">Если целевое веб-приложение не существует, оно будет автоматически создано в плане служб приложений, заданном в TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="e1b9a-112">Параметр ключа RestoreContentOnly можно использовать для восстановления только удаленных файлов приложения без параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="e1b9a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1b9a-113">EXAMPLES</span></span>

### <span data-ttu-id="e1b9a-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1b9a-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="e1b9a-115">Восстанавливает удаленное приложение с именем ContosoApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="e1b9a-116">Новое приложение с тем же именем и группой ресурсов будет создано в плане служб приложений с именем ContosoPlan, и в него будут восстановлены файлы и параметры удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="e1b9a-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e1b9a-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="e1b9a-118">Восстанавливает промежуточный слот для удаленного приложения с именем ContosoApp, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="e1b9a-119">Веб-приложение ContosoRestore, которое принадлежит к группе ресурсов Default-Web-EastUS, будет переписано.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="e1b9a-120">Удаленные параметры веб-приложения не будут восстановлены.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="e1b9a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1b9a-121">PARAMETERS</span></span>

### <span data-ttu-id="e1b9a-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1b9a-122">-AsJob</span></span>
<span data-ttu-id="e1b9a-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e1b9a-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1b9a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b9a-124">-DefaultProfile</span></span>
<span data-ttu-id="e1b9a-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1b9a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e1b9a-126">-Force</span></span>
<span data-ttu-id="e1b9a-127">Выполнение восстановления без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e1b9a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1b9a-128">-InputObject</span></span>
<span data-ttu-id="e1b9a-129">Удаленное веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-129">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="e1b9a-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1b9a-130">-Name</span></span>
<span data-ttu-id="e1b9a-131">Имя удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-131">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="e1b9a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1b9a-132">-ResourceGroupName</span></span>
<span data-ttu-id="e1b9a-133">Группа ресурсов удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-133">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="e1b9a-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="e1b9a-134">-RestoreContentOnly</span></span>
<span data-ttu-id="e1b9a-135">Восстановите файлы веб-приложения, но не восстанавливайте параметры.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="e1b9a-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="e1b9a-136">-Slot</span></span>
<span data-ttu-id="e1b9a-137">Удаленная область веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-137">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="e1b9a-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="e1b9a-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="e1b9a-139">План служб приложений для нового веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-139">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="e1b9a-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="e1b9a-140">-TargetName</span></span>
<span data-ttu-id="e1b9a-141">Имя нового веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-141">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="e1b9a-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1b9a-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="e1b9a-143">Группа ресурсов, содержащая новое веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-143">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="e1b9a-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="e1b9a-144">-TargetSlot</span></span>
<span data-ttu-id="e1b9a-145">Имя новой области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-145">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="e1b9a-146">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="e1b9a-146">-UseDisasterRecovery</span></span>
<span data-ttu-id="e1b9a-147">Используйте для восстановления удаленного приложения из неподключенного устройства масштабирования.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-147">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="e1b9a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1b9a-148">-Confirm</span></span>
<span data-ttu-id="e1b9a-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b9a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b9a-150">-WhatIf</span></span>
<span data-ttu-id="e1b9a-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1b9a-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b9a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b9a-153">CommonParameters</span></span>
<span data-ttu-id="e1b9a-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1b9a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b9a-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1b9a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b9a-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1b9a-156">INPUTS</span></span>

### <span data-ttu-id="e1b9a-157">Microsoft. Azure. Commands. Apps. командлеты. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e1b9a-157">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="e1b9a-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1b9a-158">OUTPUTS</span></span>

### <span data-ttu-id="e1b9a-159">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="e1b9a-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e1b9a-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1b9a-160">NOTES</span></span>

## <span data-ttu-id="e1b9a-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1b9a-161">RELATED LINKS</span></span>

[<span data-ttu-id="e1b9a-162">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e1b9a-162">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)