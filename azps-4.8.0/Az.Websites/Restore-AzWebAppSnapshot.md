---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236907"
---
# <span data-ttu-id="b25dc-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b25dc-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="b25dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b25dc-102">SYNOPSIS</span></span>
<span data-ttu-id="b25dc-103">Восстанавливает снимок веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b25dc-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="b25dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b25dc-104">SYNTAX</span></span>

### <span data-ttu-id="b25dc-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b25dc-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b25dc-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b25dc-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b25dc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b25dc-107">DESCRIPTION</span></span>
<span data-ttu-id="b25dc-108">Восстанавливает снимок веб-приложения в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="b25dc-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="b25dc-109">При восстановлении моментального снимка все файлы в веб-приложении перезаписываются файлами, содержащимися в снимке.</span><span class="sxs-lookup"><span data-stu-id="b25dc-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="b25dc-110">Чтобы восстановить параметры, используйте параметр ключа RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b25dc-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="b25dc-111">Вы можете восстановить моментальный снимок из одного веб-приложения в любом другом веб-приложении в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="b25dc-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="b25dc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b25dc-112">EXAMPLES</span></span>

### <span data-ttu-id="b25dc-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b25dc-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="b25dc-114">Получает последний снимок веб-приложения с именем "ContosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS".</span><span class="sxs-lookup"><span data-stu-id="b25dc-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="b25dc-115">Восстанавливает снимок в слоте "восстановление" веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b25dc-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="b25dc-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b25dc-116">PARAMETERS</span></span>

### <span data-ttu-id="b25dc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b25dc-117">-AsJob</span></span>
<span data-ttu-id="b25dc-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b25dc-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b25dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25dc-119">-DefaultProfile</span></span>
<span data-ttu-id="b25dc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b25dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b25dc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b25dc-121">-Force</span></span>
<span data-ttu-id="b25dc-122">Позволяет исходному веб-приложению быть переписано без отображения предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b25dc-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="b25dc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b25dc-123">-InputObject</span></span>
<span data-ttu-id="b25dc-124">Снимок веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b25dc-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="b25dc-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b25dc-125">-Name</span></span>
<span data-ttu-id="b25dc-126">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b25dc-126">The name of the web app.</span></span>

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

### <span data-ttu-id="b25dc-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="b25dc-127">-RecoverConfiguration</span></span>
<span data-ttu-id="b25dc-128">Восстановление конфигурации веб-приложения в дополнение к файлам.</span><span class="sxs-lookup"><span data-stu-id="b25dc-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="b25dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b25dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="b25dc-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b25dc-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b25dc-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="b25dc-131">-Slot</span></span>
<span data-ttu-id="b25dc-132">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b25dc-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b25dc-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="b25dc-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="b25dc-134">Используется для восстановления моментального снимка из неподключенного устройства масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b25dc-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="b25dc-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b25dc-135">-WebApp</span></span>
<span data-ttu-id="b25dc-136">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b25dc-136">The web app object</span></span>

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

### <span data-ttu-id="b25dc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b25dc-137">-Confirm</span></span>
<span data-ttu-id="b25dc-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b25dc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b25dc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b25dc-139">-WhatIf</span></span>
<span data-ttu-id="b25dc-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b25dc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b25dc-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b25dc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b25dc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25dc-142">CommonParameters</span></span>
<span data-ttu-id="b25dc-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b25dc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25dc-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25dc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25dc-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b25dc-145">INPUTS</span></span>

### <span data-ttu-id="b25dc-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b25dc-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b25dc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b25dc-147">System.String</span></span>

### <span data-ttu-id="b25dc-148">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="b25dc-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="b25dc-149">Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b25dc-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="b25dc-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b25dc-150">OUTPUTS</span></span>

### <span data-ttu-id="b25dc-151">System. void</span><span class="sxs-lookup"><span data-stu-id="b25dc-151">System.Void</span></span>

## <span data-ttu-id="b25dc-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="b25dc-152">NOTES</span></span>

## <span data-ttu-id="b25dc-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b25dc-153">RELATED LINKS</span></span>
