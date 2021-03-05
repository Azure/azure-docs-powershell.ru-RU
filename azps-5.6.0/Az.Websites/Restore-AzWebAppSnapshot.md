---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: be3958e44d3e5192fc9d6f7370b58fa08bde75ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002040"
---
# <span data-ttu-id="2cbdb-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2cbdb-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="2cbdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cbdb-102">SYNOPSIS</span></span>
<span data-ttu-id="2cbdb-103">Восстановление моментального снимка веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="2cbdb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2cbdb-104">SYNTAX</span></span>

### <span data-ttu-id="2cbdb-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2cbdb-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cbdb-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2cbdb-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cbdb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cbdb-107">DESCRIPTION</span></span>
<span data-ttu-id="2cbdb-108">Восстановление моментального снимка веб-приложения в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="2cbdb-109">При восстановлении моментального снимка переописыются все файлы в веб-приложении, содержащиеся в нем файлы.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="2cbdb-110">Чтобы восстановить параметры, также используйте параметр Параметр RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="2cbdb-111">Моментальный снимок из одного веб-приложения можно восстановить в любом другом веб-приложении, доступном по той же подписке.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="2cbdb-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2cbdb-112">EXAMPLES</span></span>

### <span data-ttu-id="2cbdb-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2cbdb-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="2cbdb-114">Получает последний снимок веб-приложения ContosoApp с слотом "Промежуточное обновление" в группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="2cbdb-115">Восстановление моментального снимка в слот "Восстановление" веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="2cbdb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cbdb-116">PARAMETERS</span></span>

### <span data-ttu-id="2cbdb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cbdb-117">-AsJob</span></span>
<span data-ttu-id="2cbdb-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2cbdb-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cbdb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cbdb-119">-DefaultProfile</span></span>
<span data-ttu-id="2cbdb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cbdb-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2cbdb-121">-Force</span></span>
<span data-ttu-id="2cbdb-122">Позволяет перезаписать исходное веб-приложение без отображения предупреждения.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbdb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cbdb-123">-InputObject</span></span>
<span data-ttu-id="2cbdb-124">Моментальный снимок Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbdb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2cbdb-125">-Name</span></span>
<span data-ttu-id="2cbdb-126">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-126">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbdb-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cbdb-127">-RecoverConfiguration</span></span>
<span data-ttu-id="2cbdb-128">Восстановив конфигурацию не только файлов, но и веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbdb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cbdb-129">-ResourceGroupName</span></span>
<span data-ttu-id="2cbdb-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbdb-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="2cbdb-131">-Slot</span></span>
<span data-ttu-id="2cbdb-132">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-132">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbdb-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="2cbdb-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="2cbdb-134">Используется для восстановления моментального снимка в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="2cbdb-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2cbdb-135">-WebApp</span></span>
<span data-ttu-id="2cbdb-136">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="2cbdb-136">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cbdb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cbdb-137">-Confirm</span></span>
<span data-ttu-id="2cbdb-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cbdb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cbdb-139">-WhatIf</span></span>
<span data-ttu-id="2cbdb-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cbdb-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cbdb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cbdb-142">CommonParameters</span></span>
<span data-ttu-id="2cbdb-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cbdb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cbdb-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cbdb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cbdb-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cbdb-145">INPUTS</span></span>

### <span data-ttu-id="2cbdb-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2cbdb-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2cbdb-147">System.String</span><span class="sxs-lookup"><span data-stu-id="2cbdb-147">System.String</span></span>

### <span data-ttu-id="2cbdb-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2cbdb-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="2cbdb-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2cbdb-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="2cbdb-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2cbdb-150">OUTPUTS</span></span>

### <span data-ttu-id="2cbdb-151">System.Void</span><span class="sxs-lookup"><span data-stu-id="2cbdb-151">System.Void</span></span>

## <span data-ttu-id="2cbdb-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2cbdb-152">NOTES</span></span>

## <span data-ttu-id="2cbdb-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cbdb-153">RELATED LINKS</span></span>
