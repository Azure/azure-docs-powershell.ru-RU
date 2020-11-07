---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 0719210cae275dc7e250e7fd14e622c51014d7c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914665"
---
# <span data-ttu-id="87133-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="87133-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="87133-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87133-102">SYNOPSIS</span></span>
<span data-ttu-id="87133-103">Восстанавливает снимок веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="87133-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87133-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87133-104">SYNTAX</span></span>

### <span data-ttu-id="87133-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="87133-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87133-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="87133-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87133-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87133-107">DESCRIPTION</span></span>
<span data-ttu-id="87133-108">Восстанавливает снимок веб-приложения в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="87133-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="87133-109">При восстановлении моментального снимка все файлы в веб-приложении перезаписываются файлами, содержащимися в снимке.</span><span class="sxs-lookup"><span data-stu-id="87133-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="87133-110">Чтобы восстановить параметры, используйте параметр ключа RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="87133-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="87133-111">Вы можете восстановить моментальный снимок из одного веб-приложения в любом другом веб-приложении в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="87133-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="87133-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87133-112">EXAMPLES</span></span>

### <span data-ttu-id="87133-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87133-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="87133-114">Получает последний снимок веб-приложения с именем "ContosoApp" и гнездом "промежуточное хранение" в группе ресурсов "Default-Web-WestUS".</span><span class="sxs-lookup"><span data-stu-id="87133-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="87133-115">Восстанавливает снимок в слоте "восстановление" веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="87133-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="87133-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87133-116">PARAMETERS</span></span>

### <span data-ttu-id="87133-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87133-117">-AsJob</span></span>
<span data-ttu-id="87133-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="87133-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87133-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87133-119">-DefaultProfile</span></span>
<span data-ttu-id="87133-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87133-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87133-121">-Force</span><span class="sxs-lookup"><span data-stu-id="87133-121">-Force</span></span>
<span data-ttu-id="87133-122">Позволяет исходному веб-приложению быть переписано без отображения предупреждения.</span><span class="sxs-lookup"><span data-stu-id="87133-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="87133-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87133-123">-InputObject</span></span>
<span data-ttu-id="87133-124">Снимок веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="87133-124">The Azure Web App snapshot.</span></span>
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

### <span data-ttu-id="87133-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87133-125">-Name</span></span>
<span data-ttu-id="87133-126">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="87133-126">The name of the web app.</span></span>
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

### <span data-ttu-id="87133-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="87133-127">-RecoverConfiguration</span></span>
<span data-ttu-id="87133-128">Восстановление конфигурации веб-приложения в дополнение к файлам.</span><span class="sxs-lookup"><span data-stu-id="87133-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="87133-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87133-129">-ResourceGroupName</span></span>
<span data-ttu-id="87133-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87133-130">The name of the resource group.</span></span>
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

### <span data-ttu-id="87133-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="87133-131">-Slot</span></span>
<span data-ttu-id="87133-132">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="87133-132">The name of the web app slot.</span></span>
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

### <span data-ttu-id="87133-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="87133-133">-WebApp</span></span>
<span data-ttu-id="87133-134">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="87133-134">The web app object</span></span>
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

### <span data-ttu-id="87133-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87133-135">-Confirm</span></span>
<span data-ttu-id="87133-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87133-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87133-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87133-137">-WhatIf</span></span>
<span data-ttu-id="87133-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87133-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87133-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87133-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87133-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87133-140">CommonParameters</span></span>
<span data-ttu-id="87133-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87133-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87133-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87133-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87133-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87133-143">INPUTS</span></span>

### <span data-ttu-id="87133-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87133-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="87133-145">Microsoft. Azure. Management. website. Models. Site System. String Microsoft. Azure. Commands. Apps. командлеты. BackupRestore. AzureWebAppSnapshot System. DateTime</span><span class="sxs-lookup"><span data-stu-id="87133-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="87133-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87133-146">OUTPUTS</span></span>

### <span data-ttu-id="87133-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="87133-147">System.Object</span></span>

## <span data-ttu-id="87133-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="87133-148">NOTES</span></span>

## <span data-ttu-id="87133-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87133-149">RELATED LINKS</span></span>

