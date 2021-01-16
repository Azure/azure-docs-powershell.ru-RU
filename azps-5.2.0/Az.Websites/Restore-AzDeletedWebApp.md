---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326034"
---
# <span data-ttu-id="ee24b-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ee24b-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="ee24b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee24b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee24b-103">Восстановление удаленного веб-приложения в новое или существующее веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="ee24b-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="ee24b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee24b-104">SYNTAX</span></span>

### <span data-ttu-id="ee24b-105">FromDeletedResourceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee24b-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee24b-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="ee24b-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee24b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee24b-107">DESCRIPTION</span></span>
<span data-ttu-id="ee24b-108">С **помощью cmdlet Restore-AzDeletedWebApp** можно восстановить удаленное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="ee24b-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="ee24b-109">Веб-приложение, заданное TargetResourceGroupName, TargetName и TargetSlot, будет перезаписано с помощью содержимого и параметров удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ee24b-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="ee24b-110">Если целевые параметры не указаны, они будут автоматически заполнены группой ресурсов, именем и слотом удаленных веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="ee24b-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="ee24b-111">Если целевое веб-приложение не существует, оно будет автоматически создано в плане обслуживания приложения, указанном в TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="ee24b-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="ee24b-112">Параметр RestoreContentOnly можно использовать для восстановления только файлов удаленного приложения без параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="ee24b-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="ee24b-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee24b-113">EXAMPLES</span></span>

### <span data-ttu-id="ee24b-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee24b-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="ee24b-115">Восстановление удаленного приложения ContosoApp, принадлежащего группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ee24b-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="ee24b-116">В плане службы приложения с именем и группой ресурсов будет создано новое приложение с именем ContosoPlan, и в него будут восстановлены файлы и параметры удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="ee24b-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="ee24b-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee24b-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="ee24b-118">Восстановление промежуточного слота удаленного приложения ContosoApp, принадлежащего группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ee24b-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="ee24b-119">Веб-приложение ContosoRestore, принадлежащее группе ресурсов Default-Web-EastUS, будет перезаписано.</span><span class="sxs-lookup"><span data-stu-id="ee24b-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="ee24b-120">Удаленные параметры веб-приложения не будут восстановлены.</span><span class="sxs-lookup"><span data-stu-id="ee24b-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="ee24b-121">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ee24b-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="ee24b-122">Если есть два удаленных приложения с одинаковым именем (ContosoApp), мы получаем сведения о сайтах и восстанавливаем приложение с именем ContosoRestore с помощью нужного приложения, позвонив на восстановление с помощью ИД.</span><span class="sxs-lookup"><span data-stu-id="ee24b-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="ee24b-123">Пример 4</span><span class="sxs-lookup"><span data-stu-id="ee24b-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="ee24b-124">Если есть два удаленных приложения с одинаковыми именами (ContosoApp), мы получаем сведения о сайтах и восстанавливаем приложение с именем ContosoRestore с помощью приложения, вызываемого восстановления с помощью InputObject(Deletedsite)</span><span class="sxs-lookup"><span data-stu-id="ee24b-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="ee24b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee24b-125">PARAMETERS</span></span>

### <span data-ttu-id="ee24b-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee24b-126">-AsJob</span></span>
<span data-ttu-id="ee24b-127">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ee24b-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee24b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee24b-128">-DefaultProfile</span></span>
<span data-ttu-id="ee24b-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee24b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee24b-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="ee24b-130">-DeletedId</span></span>
<span data-ttu-id="ee24b-131">ИД удаленного приложения Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="ee24b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="ee24b-132">-Force</span></span>
<span data-ttu-id="ee24b-133">Восстановление можно сделать без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ee24b-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ee24b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee24b-134">-InputObject</span></span>
<span data-ttu-id="ee24b-135">Удалено приложение Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="ee24b-136">-Location</span><span class="sxs-lookup"><span data-stu-id="ee24b-136">-Location</span></span>
<span data-ttu-id="ee24b-137">Расположение удаленного приложения Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="ee24b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="ee24b-138">-Name</span></span>
<span data-ttu-id="ee24b-139">Имя удаленного приложения Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="ee24b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee24b-140">-ResourceGroupName</span></span>
<span data-ttu-id="ee24b-141">Группа ресурсов удаленного приложения Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="ee24b-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="ee24b-142">-RestoreContentOnly</span></span>
<span data-ttu-id="ee24b-143">Восстановление файлов веб-приложения без восстановления параметров.</span><span class="sxs-lookup"><span data-stu-id="ee24b-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="ee24b-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="ee24b-144">-Slot</span></span>
<span data-ttu-id="ee24b-145">Удаленный слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="ee24b-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="ee24b-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="ee24b-147">План обслуживания приложения для нового приложения Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="ee24b-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="ee24b-148">-TargetName</span></span>
<span data-ttu-id="ee24b-149">Имя нового приложения Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="ee24b-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee24b-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="ee24b-151">Группа ресурсов, содержащая новую службу Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="ee24b-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="ee24b-152">-TargetSlot</span></span>
<span data-ttu-id="ee24b-153">Название нового слота Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ee24b-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="ee24b-154">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="ee24b-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="ee24b-155">Используется для восстановления удаленного приложения в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="ee24b-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="ee24b-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee24b-156">-Confirm</span></span>
<span data-ttu-id="ee24b-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee24b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee24b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee24b-158">-WhatIf</span></span>
<span data-ttu-id="ee24b-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee24b-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee24b-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ee24b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee24b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee24b-161">CommonParameters</span></span>
<span data-ttu-id="ee24b-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee24b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee24b-163">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee24b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee24b-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee24b-164">INPUTS</span></span>

### <span data-ttu-id="ee24b-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ee24b-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="ee24b-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee24b-166">OUTPUTS</span></span>

### <span data-ttu-id="ee24b-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ee24b-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ee24b-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee24b-168">NOTES</span></span>

## <span data-ttu-id="ee24b-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee24b-169">RELATED LINKS</span></span>

[<span data-ttu-id="ee24b-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ee24b-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)