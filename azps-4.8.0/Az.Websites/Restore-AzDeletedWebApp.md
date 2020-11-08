---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236908"
---
# <span data-ttu-id="d8bd2-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d8bd2-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="d8bd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="d8bd2-103">Восстанавливает удаленное веб-приложение в новом или существующем веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="d8bd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8bd2-104">SYNTAX</span></span>

### <span data-ttu-id="d8bd2-105">FromDeletedResourceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8bd2-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8bd2-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="d8bd2-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8bd2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8bd2-107">DESCRIPTION</span></span>
<span data-ttu-id="d8bd2-108">Командлет **RESTORE-AzDeletedWebApp** восстанавливает удаленное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="d8bd2-109">Веб-приложение, указанное в TargetResourceGroupName, TargetName и TargetSlot, будет заменено содержимым и параметрами удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="d8bd2-110">Если целевые параметры не заданы, они будут автоматически заполнены группой ресурсов, именем и областью удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="d8bd2-111">Если целевое веб-приложение не существует, оно будет автоматически создано в плане служб приложений, заданном в TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="d8bd2-112">Параметр ключа RestoreContentOnly можно использовать для восстановления только удаленных файлов приложения без параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="d8bd2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8bd2-113">EXAMPLES</span></span>

### <span data-ttu-id="d8bd2-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8bd2-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="d8bd2-115">Восстанавливает удаленное приложение с именем ContosoApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d8bd2-116">Новое приложение с тем же именем и группой ресурсов будет создано в плане служб приложений с именем ContosoPlan, и в него будут восстановлены файлы и параметры удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="d8bd2-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d8bd2-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="d8bd2-118">Восстанавливает промежуточный слот для удаленного приложения с именем ContosoApp, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="d8bd2-119">Веб-приложение ContosoRestore, которое принадлежит к группе ресурсов Default-Web-EastUS, будет переписано.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="d8bd2-120">Удаленные параметры веб-приложения не будут восстановлены.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="d8bd2-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d8bd2-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="d8bd2-122">В случае 2 удаленных приложений с одинаковым именем (ContosoApp) мы получаем сведения о сайтах и восстанавливайте приложение с именем ContosoRestore с помощью вызова Restore с идентификатором.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="d8bd2-123">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d8bd2-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="d8bd2-124">В случае 2 удаленных приложений с одинаковым именем (ContosoApp), мы получаем сведения о сайтах и восстанавливайте приложение с именем ContosoRestore с помощью приложения нашего выбора, вызывая восстановление с помощью параметра InputObject (Deletedsite).</span><span class="sxs-lookup"><span data-stu-id="d8bd2-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="d8bd2-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8bd2-125">PARAMETERS</span></span>

### <span data-ttu-id="d8bd2-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8bd2-126">-AsJob</span></span>
<span data-ttu-id="d8bd2-127">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d8bd2-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8bd2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8bd2-128">-DefaultProfile</span></span>
<span data-ttu-id="d8bd2-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8bd2-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="d8bd2-130">-DeletedId</span></span>
<span data-ttu-id="d8bd2-131">Идентификатор удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="d8bd2-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d8bd2-132">-Force</span></span>
<span data-ttu-id="d8bd2-133">Выполнение восстановления без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d8bd2-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8bd2-134">-InputObject</span></span>
<span data-ttu-id="d8bd2-135">Удаленное веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="d8bd2-136">-Location</span><span class="sxs-lookup"><span data-stu-id="d8bd2-136">-Location</span></span>
<span data-ttu-id="d8bd2-137">Расположение удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="d8bd2-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8bd2-138">-Name</span></span>
<span data-ttu-id="d8bd2-139">Имя удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="d8bd2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8bd2-140">-ResourceGroupName</span></span>
<span data-ttu-id="d8bd2-141">Группа ресурсов удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="d8bd2-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="d8bd2-142">-RestoreContentOnly</span></span>
<span data-ttu-id="d8bd2-143">Восстановите файлы веб-приложения, но не восстанавливайте параметры.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="d8bd2-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="d8bd2-144">-Slot</span></span>
<span data-ttu-id="d8bd2-145">Удаленная область веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="d8bd2-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="d8bd2-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="d8bd2-147">План служб приложений для нового веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="d8bd2-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="d8bd2-148">-TargetName</span></span>
<span data-ttu-id="d8bd2-149">Имя нового веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="d8bd2-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8bd2-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="d8bd2-151">Группа ресурсов, содержащая новое веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="d8bd2-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="d8bd2-152">-TargetSlot</span></span>
<span data-ttu-id="d8bd2-153">Имя новой области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="d8bd2-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="d8bd2-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="d8bd2-155">Используйте для восстановления удаленного приложения из неподключенного устройства масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="d8bd2-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8bd2-156">-Confirm</span></span>
<span data-ttu-id="d8bd2-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8bd2-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8bd2-158">-WhatIf</span></span>
<span data-ttu-id="d8bd2-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8bd2-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8bd2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8bd2-161">CommonParameters</span></span>
<span data-ttu-id="d8bd2-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8bd2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8bd2-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8bd2-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8bd2-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8bd2-164">INPUTS</span></span>

### <span data-ttu-id="d8bd2-165">Microsoft. Azure. Commands. Apps. командлеты. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d8bd2-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="d8bd2-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8bd2-166">OUTPUTS</span></span>

### <span data-ttu-id="d8bd2-167">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="d8bd2-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d8bd2-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8bd2-168">NOTES</span></span>

## <span data-ttu-id="d8bd2-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8bd2-169">RELATED LINKS</span></span>

[<span data-ttu-id="d8bd2-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d8bd2-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)