---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 9a90e56909de016bb388be1a43f5b41c8e47e9e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913541"
---
# <span data-ttu-id="d42c2-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d42c2-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d42c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d42c2-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d42c2-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d42c2-103">SYNTAX</span></span>

### <span data-ttu-id="d42c2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d42c2-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="d42c2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d42c2-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="d42c2-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d42c2-106">DESCRIPTION</span></span>
<span data-ttu-id="d42c2-107">Командлет **Edit-AzureRmWebAppBackupConfiguration** редактирует текущую резервную копию конфигурации для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="d42c2-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="d42c2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d42c2-108">EXAMPLES</span></span>

## <span data-ttu-id="d42c2-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d42c2-109">PARAMETERS</span></span>

### <span data-ttu-id="d42c2-110">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="d42c2-110">-Databases</span></span>
<span data-ttu-id="d42c2-111">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="d42c2-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="d42c2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d42c2-112">-DefaultProfile</span></span>
<span data-ttu-id="d42c2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d42c2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d42c2-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="d42c2-114">-FrequencyInterval</span></span>
<span data-ttu-id="d42c2-115">Интервал частот</span><span class="sxs-lookup"><span data-stu-id="d42c2-115">Frequency Interval</span></span>

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

### <span data-ttu-id="d42c2-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="d42c2-116">-FrequencyUnit</span></span>
<span data-ttu-id="d42c2-117">Частотный блок</span><span class="sxs-lookup"><span data-stu-id="d42c2-117">Frequency Unit</span></span>

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

### <span data-ttu-id="d42c2-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="d42c2-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="d42c2-119">Сохранить хотя бы один вариант резервного копирования</span><span class="sxs-lookup"><span data-stu-id="d42c2-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="d42c2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d42c2-120">-Name</span></span>
<span data-ttu-id="d42c2-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="d42c2-121">WebApp Name</span></span>

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

### <span data-ttu-id="d42c2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d42c2-122">-ResourceGroupName</span></span>
<span data-ttu-id="d42c2-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d42c2-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d42c2-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="d42c2-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="d42c2-125">Срок хранения в днях</span><span class="sxs-lookup"><span data-stu-id="d42c2-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="d42c2-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="d42c2-126">-Slot</span></span>
<span data-ttu-id="d42c2-127">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="d42c2-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d42c2-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d42c2-128">-StartTime</span></span>
<span data-ttu-id="d42c2-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="d42c2-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="d42c2-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="d42c2-130">-StorageAccountUrl</span></span>
<span data-ttu-id="d42c2-131">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d42c2-131">Storage Account Url</span></span>

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

### <span data-ttu-id="d42c2-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d42c2-132">-WebApp</span></span>
<span data-ttu-id="d42c2-133">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="d42c2-133">WebApp Object</span></span>

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

### <span data-ttu-id="d42c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d42c2-134">CommonParameters</span></span>
<span data-ttu-id="d42c2-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d42c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d42c2-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d42c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d42c2-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d42c2-137">INPUTS</span></span>

### <span data-ttu-id="d42c2-138">Семейств</span><span class="sxs-lookup"><span data-stu-id="d42c2-138">Site</span></span>
<span data-ttu-id="d42c2-139">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d42c2-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d42c2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d42c2-140">OUTPUTS</span></span>

### <span data-ttu-id="d42c2-141">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d42c2-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d42c2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d42c2-142">NOTES</span></span>

## <span data-ttu-id="d42c2-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d42c2-143">RELATED LINKS</span></span>

[<span data-ttu-id="d42c2-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d42c2-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


