---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4319a2637b2dbb008056a6b369ace539b889cd37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728380"
---
# <span data-ttu-id="d5fde-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5fde-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d5fde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5fde-102">SYNOPSIS</span></span>

## <span data-ttu-id="d5fde-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5fde-103">SYNTAX</span></span>

### <span data-ttu-id="d5fde-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d5fde-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="d5fde-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d5fde-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="d5fde-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5fde-106">DESCRIPTION</span></span>
<span data-ttu-id="d5fde-107">Командлет **Edit-AzWebAppBackupConfiguration** редактирует текущую резервную копию конфигурации для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fde-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="d5fde-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5fde-108">EXAMPLES</span></span>

## <span data-ttu-id="d5fde-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5fde-109">PARAMETERS</span></span>

### <span data-ttu-id="d5fde-110">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="d5fde-110">-Databases</span></span>
<span data-ttu-id="d5fde-111">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="d5fde-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fde-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fde-112">-DefaultProfile</span></span>
<span data-ttu-id="d5fde-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fde-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5fde-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="d5fde-114">-FrequencyInterval</span></span>
<span data-ttu-id="d5fde-115">Интервал частот</span><span class="sxs-lookup"><span data-stu-id="d5fde-115">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fde-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="d5fde-116">-FrequencyUnit</span></span>
<span data-ttu-id="d5fde-117">Частотный блок</span><span class="sxs-lookup"><span data-stu-id="d5fde-117">Frequency Unit</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fde-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="d5fde-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="d5fde-119">Сохранить хотя бы один вариант резервного копирования</span><span class="sxs-lookup"><span data-stu-id="d5fde-119">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fde-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5fde-120">-Name</span></span>
<span data-ttu-id="d5fde-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="d5fde-121">WebApp Name</span></span>

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

### <span data-ttu-id="d5fde-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5fde-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5fde-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d5fde-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d5fde-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="d5fde-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="d5fde-125">Срок хранения в днях</span><span class="sxs-lookup"><span data-stu-id="d5fde-125">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fde-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="d5fde-126">-Slot</span></span>
<span data-ttu-id="d5fde-127">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="d5fde-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d5fde-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d5fde-128">-StartTime</span></span>
<span data-ttu-id="d5fde-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="d5fde-129">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fde-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="d5fde-130">-StorageAccountUrl</span></span>
<span data-ttu-id="d5fde-131">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d5fde-131">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fde-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d5fde-132">-WebApp</span></span>
<span data-ttu-id="d5fde-133">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="d5fde-133">WebApp Object</span></span>

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

### <span data-ttu-id="d5fde-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fde-134">CommonParameters</span></span>
<span data-ttu-id="d5fde-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5fde-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fde-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5fde-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fde-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5fde-137">INPUTS</span></span>

### <span data-ttu-id="d5fde-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d5fde-138">System.Int32</span></span>

### <span data-ttu-id="d5fde-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d5fde-139">System.String</span></span>

### <span data-ttu-id="d5fde-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d5fde-140">System.DateTime</span></span>

### <span data-ttu-id="d5fde-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d5fde-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d5fde-142">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="d5fde-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="d5fde-143">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="d5fde-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="d5fde-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5fde-144">OUTPUTS</span></span>

### <span data-ttu-id="d5fde-145">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5fde-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d5fde-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5fde-146">NOTES</span></span>

## <span data-ttu-id="d5fde-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5fde-147">RELATED LINKS</span></span>

[<span data-ttu-id="d5fde-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5fde-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


