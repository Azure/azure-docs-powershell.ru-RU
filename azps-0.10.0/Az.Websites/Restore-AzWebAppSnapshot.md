---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: bd7c967bce709c1951cc7a61c1f8bfab9c78f28a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910570"
---
# <span data-ttu-id="f1a24-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f1a24-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="f1a24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1a24-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a24-103">Восстанавливает снимок веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f1a24-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="f1a24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1a24-104">SYNTAX</span></span>

### <span data-ttu-id="f1a24-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f1a24-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a24-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f1a24-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1a24-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1a24-107">DESCRIPTION</span></span>
<span data-ttu-id="f1a24-108">Восстанавливает снимок веб-приложения в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="f1a24-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="f1a24-109">При восстановлении моментального снимка все файлы в веб-приложении перезаписываются файлами, содержащимися в снимке.</span><span class="sxs-lookup"><span data-stu-id="f1a24-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="f1a24-110">Чтобы восстановить параметры, используйте параметр ключа RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1a24-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="f1a24-111">Вы можете восстановить моментальный снимок из одного веб-приложения в любом другом веб-приложении в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="f1a24-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="f1a24-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1a24-112">EXAMPLES</span></span>

### <span data-ttu-id="f1a24-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1a24-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="f1a24-114">Получает последний снимок веб-приложения с именем "ContosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS".</span><span class="sxs-lookup"><span data-stu-id="f1a24-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="f1a24-115">Восстанавливает снимок в слоте "восстановление" веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f1a24-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="f1a24-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1a24-116">PARAMETERS</span></span>

### <span data-ttu-id="f1a24-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1a24-117">-AsJob</span></span>
<span data-ttu-id="f1a24-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f1a24-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1a24-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a24-119">-DefaultProfile</span></span>
<span data-ttu-id="f1a24-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a24-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f1a24-121">-Force</span></span>
<span data-ttu-id="f1a24-122">Позволяет исходному веб-приложению быть переписано без отображения предупреждения.</span><span class="sxs-lookup"><span data-stu-id="f1a24-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1a24-123">-InputObject</span></span>
<span data-ttu-id="f1a24-124">Снимок веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a24-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1a24-125">-Name</span></span>
<span data-ttu-id="f1a24-126">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f1a24-126">The name of the web app.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1a24-127">-RecoverConfiguration</span></span>
<span data-ttu-id="f1a24-128">Восстановление конфигурации веб-приложения в дополнение к файлам.</span><span class="sxs-lookup"><span data-stu-id="f1a24-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a24-129">-ResourceGroupName</span></span>
<span data-ttu-id="f1a24-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1a24-130">The name of the resource group.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="f1a24-131">-Slot</span></span>
<span data-ttu-id="f1a24-132">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f1a24-132">The name of the web app slot.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f1a24-133">-WebApp</span></span>
<span data-ttu-id="f1a24-134">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="f1a24-134">The web app object</span></span>
```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1a24-135">-Confirm</span></span>
<span data-ttu-id="f1a24-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1a24-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a24-137">-WhatIf</span></span>
<span data-ttu-id="f1a24-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1a24-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a24-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1a24-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a24-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a24-140">CommonParameters</span></span>
<span data-ttu-id="f1a24-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1a24-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a24-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a24-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a24-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1a24-143">INPUTS</span></span>

### <span data-ttu-id="f1a24-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1a24-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="f1a24-145">Microsoft. Azure. Management. website. Models. Site System. String Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot System. DateTime</span><span class="sxs-lookup"><span data-stu-id="f1a24-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="f1a24-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1a24-146">OUTPUTS</span></span>

### <span data-ttu-id="f1a24-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="f1a24-147">System.Object</span></span>

## <span data-ttu-id="f1a24-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1a24-148">NOTES</span></span>

## <span data-ttu-id="f1a24-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1a24-149">RELATED LINKS</span></span>

