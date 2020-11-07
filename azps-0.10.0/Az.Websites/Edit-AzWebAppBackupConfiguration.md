---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/edit-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: cfac8f1cd3d25ff630900bb5d7723e713b3d4c65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910636"
---
# <span data-ttu-id="39e79-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="39e79-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="39e79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39e79-102">SYNOPSIS</span></span>

## <span data-ttu-id="39e79-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39e79-103">SYNTAX</span></span>

### <span data-ttu-id="39e79-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="39e79-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="39e79-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="39e79-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="39e79-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39e79-106">DESCRIPTION</span></span>
<span data-ttu-id="39e79-107">Командлет **Edit-AzWebAppBackupConfiguration** редактирует текущую резервную копию конфигурации для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="39e79-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="39e79-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39e79-108">EXAMPLES</span></span>

## <span data-ttu-id="39e79-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39e79-109">PARAMETERS</span></span>

### <span data-ttu-id="39e79-110">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="39e79-110">-Databases</span></span>
<span data-ttu-id="39e79-111">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="39e79-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e79-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e79-112">-DefaultProfile</span></span>
<span data-ttu-id="39e79-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39e79-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39e79-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="39e79-114">-FrequencyInterval</span></span>
<span data-ttu-id="39e79-115">Интервал частот</span><span class="sxs-lookup"><span data-stu-id="39e79-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e79-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="39e79-116">-FrequencyUnit</span></span>
<span data-ttu-id="39e79-117">Частотный блок</span><span class="sxs-lookup"><span data-stu-id="39e79-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e79-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="39e79-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="39e79-119">Сохранить хотя бы один вариант резервного копирования</span><span class="sxs-lookup"><span data-stu-id="39e79-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e79-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="39e79-120">-Name</span></span>
<span data-ttu-id="39e79-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="39e79-121">WebApp Name</span></span>

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

### <span data-ttu-id="39e79-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e79-122">-ResourceGroupName</span></span>
<span data-ttu-id="39e79-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="39e79-123">Resource Group Name</span></span>

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

### <span data-ttu-id="39e79-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="39e79-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="39e79-125">Срок хранения в днях</span><span class="sxs-lookup"><span data-stu-id="39e79-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e79-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="39e79-126">-Slot</span></span>
<span data-ttu-id="39e79-127">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="39e79-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="39e79-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="39e79-128">-StartTime</span></span>
<span data-ttu-id="39e79-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="39e79-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e79-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="39e79-130">-StorageAccountUrl</span></span>
<span data-ttu-id="39e79-131">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="39e79-131">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e79-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="39e79-132">-WebApp</span></span>
<span data-ttu-id="39e79-133">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="39e79-133">WebApp Object</span></span>

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

### <span data-ttu-id="39e79-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e79-134">CommonParameters</span></span>
<span data-ttu-id="39e79-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39e79-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e79-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e79-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e79-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39e79-137">INPUTS</span></span>

### <span data-ttu-id="39e79-138">Семейств</span><span class="sxs-lookup"><span data-stu-id="39e79-138">Site</span></span>
<span data-ttu-id="39e79-139">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="39e79-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="39e79-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39e79-140">OUTPUTS</span></span>

### <span data-ttu-id="39e79-141">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="39e79-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="39e79-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="39e79-142">NOTES</span></span>

## <span data-ttu-id="39e79-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39e79-143">RELATED LINKS</span></span>

[<span data-ttu-id="39e79-144">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="39e79-144">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


