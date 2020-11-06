---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562483"
---
# <span data-ttu-id="b6334-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b6334-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="b6334-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6334-102">SYNOPSIS</span></span>
<span data-ttu-id="b6334-103">Восстанавливает снимок веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b6334-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6334-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6334-104">SYNTAX</span></span>

### <span data-ttu-id="b6334-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b6334-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6334-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b6334-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6334-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6334-107">DESCRIPTION</span></span>
<span data-ttu-id="b6334-108">Восстанавливает снимок веб-приложения в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="b6334-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="b6334-109">При восстановлении моментального снимка все файлы в веб-приложении перезаписываются файлами, содержащимися в снимке.</span><span class="sxs-lookup"><span data-stu-id="b6334-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="b6334-110">Чтобы восстановить параметры, используйте параметр ключа RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b6334-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="b6334-111">Вы можете восстановить моментальный снимок из одного веб-приложения в любом другом веб-приложении в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="b6334-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="b6334-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6334-112">EXAMPLES</span></span>

### <span data-ttu-id="b6334-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6334-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="b6334-114">Получает последний снимок веб-приложения с именем "ContosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS".</span><span class="sxs-lookup"><span data-stu-id="b6334-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="b6334-115">Восстанавливает снимок в слоте "восстановление" веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b6334-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="b6334-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6334-116">PARAMETERS</span></span>

### <span data-ttu-id="b6334-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6334-117">-AsJob</span></span>
<span data-ttu-id="b6334-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b6334-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6334-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6334-119">-DefaultProfile</span></span>
<span data-ttu-id="b6334-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6334-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6334-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b6334-121">-Force</span></span>
<span data-ttu-id="b6334-122">Позволяет исходному веб-приложению быть переписано без отображения предупреждения.</span><span class="sxs-lookup"><span data-stu-id="b6334-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="b6334-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6334-123">-InputObject</span></span>
<span data-ttu-id="b6334-124">Снимок веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b6334-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="b6334-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6334-125">-Name</span></span>
<span data-ttu-id="b6334-126">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b6334-126">The name of the web app.</span></span>

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

### <span data-ttu-id="b6334-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6334-127">-RecoverConfiguration</span></span>
<span data-ttu-id="b6334-128">Восстановление конфигурации веб-приложения в дополнение к файлам.</span><span class="sxs-lookup"><span data-stu-id="b6334-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="b6334-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6334-129">-ResourceGroupName</span></span>
<span data-ttu-id="b6334-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6334-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b6334-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="b6334-131">-Slot</span></span>
<span data-ttu-id="b6334-132">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="b6334-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b6334-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b6334-133">-WebApp</span></span>
<span data-ttu-id="b6334-134">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="b6334-134">The web app object</span></span>

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

### <span data-ttu-id="b6334-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6334-135">-Confirm</span></span>
<span data-ttu-id="b6334-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6334-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6334-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6334-137">-WhatIf</span></span>
<span data-ttu-id="b6334-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6334-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6334-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6334-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6334-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6334-140">CommonParameters</span></span>
<span data-ttu-id="b6334-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6334-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6334-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6334-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6334-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6334-143">INPUTS</span></span>

### <span data-ttu-id="b6334-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6334-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b6334-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b6334-145">System.String</span></span>

### <span data-ttu-id="b6334-146">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="b6334-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="b6334-147">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6334-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="b6334-148">Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b6334-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="b6334-149">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b6334-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b6334-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6334-150">OUTPUTS</span></span>

### <span data-ttu-id="b6334-151">System. void</span><span class="sxs-lookup"><span data-stu-id="b6334-151">System.Void</span></span>

## <span data-ttu-id="b6334-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6334-152">NOTES</span></span>

## <span data-ttu-id="b6334-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6334-153">RELATED LINKS</span></span>
