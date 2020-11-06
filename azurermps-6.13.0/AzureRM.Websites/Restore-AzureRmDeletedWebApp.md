---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565276"
---
# <span data-ttu-id="05f5d-101">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="05f5d-101">Restore-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="05f5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="05f5d-103">Восстанавливает удаленное веб-приложение в новом или существующем веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="05f5d-103">Restores a deleted web app to a new or existing web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05f5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05f5d-104">SYNTAX</span></span>

### <span data-ttu-id="05f5d-105">FromDeletedResourceName</span><span class="sxs-lookup"><span data-stu-id="05f5d-105">FromDeletedResourceName</span></span>
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05f5d-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="05f5d-106">FromDeletedApp</span></span>
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## <span data-ttu-id="05f5d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05f5d-107">DESCRIPTION</span></span>
<span data-ttu-id="05f5d-108">Командлет **RESTORE-AzureRmDeletedWebApp** восстанавливает удаленное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="05f5d-108">The **Restore-AzureRmDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="05f5d-109">Веб-приложение, указанное в TargetResourceGroupName, TargetName и TargetSlot, будет заменено содержимым и параметрами удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="05f5d-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="05f5d-110">Если целевые параметры не заданы, они будут автоматически заполнены группой ресурсов, именем и областью удаленного веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="05f5d-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="05f5d-111">Если целевое веб-приложение не существует, оно будет автоматически создано в плане служб приложений, заданном в TargetAppServicePlanName.</span><span class="sxs-lookup"><span data-stu-id="05f5d-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="05f5d-112">Параметр ключа RestoreContentOnly можно использовать для восстановления только удаленных файлов приложения без параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="05f5d-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="05f5d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05f5d-113">EXAMPLES</span></span>

### <span data-ttu-id="05f5d-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05f5d-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="05f5d-115">Восстанавливает удаленное приложение с именем ContosoApp, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="05f5d-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="05f5d-116">Новое приложение с тем же именем и группой ресурсов будет создано в плане служб приложений с именем ContosoPlan, и в него будут восстановлены файлы и параметры удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="05f5d-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="05f5d-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="05f5d-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="05f5d-118">Восстанавливает промежуточный слот для удаленного приложения с именем ContosoApp, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="05f5d-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="05f5d-119">Веб-приложение ContosoRestore, которое принадлежит к группе ресурсов Default-Web-EastUS, будет переписано.</span><span class="sxs-lookup"><span data-stu-id="05f5d-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="05f5d-120">Удаленные параметры веб-приложения не будут восстановлены.</span><span class="sxs-lookup"><span data-stu-id="05f5d-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="05f5d-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05f5d-121">PARAMETERS</span></span>

### <span data-ttu-id="05f5d-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05f5d-122">-AsJob</span></span>
<span data-ttu-id="05f5d-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="05f5d-123">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f5d-124">-DefaultProfile</span></span>
<span data-ttu-id="05f5d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="05f5d-126">-Force</span></span>
<span data-ttu-id="05f5d-127">Выполнение восстановления без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="05f5d-127">Do the restore without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05f5d-128">-InputObject</span></span>
<span data-ttu-id="05f5d-129">Удаленное веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-129">The deleted Azure Web App.</span></span>

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05f5d-130">-Name</span></span>
<span data-ttu-id="05f5d-131">Имя удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f5d-132">-ResourceGroupName</span></span>
<span data-ttu-id="05f5d-133">Группа ресурсов удаленного веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="05f5d-134">-RestoreContentOnly</span></span>
<span data-ttu-id="05f5d-135">Восстановите файлы веб-приложения, но не восстанавливайте параметры.</span><span class="sxs-lookup"><span data-stu-id="05f5d-135">Restore the web app's files, but do not restore the settings.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="05f5d-136">-Slot</span></span>
<span data-ttu-id="05f5d-137">Удаленная область веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="05f5d-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="05f5d-139">План служб приложений для нового веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-139">The App Service Plan for the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="05f5d-140">-TargetName</span></span>
<span data-ttu-id="05f5d-141">Имя нового веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-141">The name of the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f5d-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="05f5d-143">Группа ресурсов, содержащая новое веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-143">The resource group containing the new Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="05f5d-144">-TargetSlot</span></span>
<span data-ttu-id="05f5d-145">Имя новой области веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="05f5d-145">The name of the new Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05f5d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f5d-146">CommonParameters</span></span>
<span data-ttu-id="05f5d-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05f5d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="05f5d-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05f5d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f5d-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05f5d-149">INPUTS</span></span>

### <span data-ttu-id="05f5d-150">Microsoft. Azure. Commands. Apps. командлеты. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="05f5d-150">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="05f5d-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05f5d-151">OUTPUTS</span></span>

### <span data-ttu-id="05f5d-152">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="05f5d-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="05f5d-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="05f5d-153">NOTES</span></span>

## <span data-ttu-id="05f5d-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05f5d-154">RELATED LINKS</span></span>

[<span data-ttu-id="05f5d-155">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="05f5d-155">Get-AzureRmDeletedWebApp</span></span>](./Get-AzureRmDeletedWebApp.md)
