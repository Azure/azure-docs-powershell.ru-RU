---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: d7fd26d81b683095fb08c1dbca3226761f047d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561983"
---
# <span data-ttu-id="9bcaf-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bcaf-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="9bcaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bcaf-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bcaf-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bcaf-103">SYNTAX</span></span>

### <span data-ttu-id="9bcaf-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9bcaf-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="9bcaf-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9bcaf-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="9bcaf-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bcaf-106">DESCRIPTION</span></span>
<span data-ttu-id="9bcaf-107">Командлет **Edit-AzureRmWebAppBackupConfiguration** редактирует текущую резервную копию конфигурации для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="9bcaf-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="9bcaf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bcaf-108">EXAMPLES</span></span>

## <span data-ttu-id="9bcaf-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bcaf-109">PARAMETERS</span></span>

### <span data-ttu-id="9bcaf-110">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="9bcaf-110">-Databases</span></span>
<span data-ttu-id="9bcaf-111">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="9bcaf-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="9bcaf-112">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="9bcaf-112">-FrequencyInterval</span></span>
<span data-ttu-id="9bcaf-113">Интервал частот</span><span class="sxs-lookup"><span data-stu-id="9bcaf-113">Frequency Interval</span></span>

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

### <span data-ttu-id="9bcaf-114">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="9bcaf-114">-FrequencyUnit</span></span>
<span data-ttu-id="9bcaf-115">Частотный блок</span><span class="sxs-lookup"><span data-stu-id="9bcaf-115">Frequency Unit</span></span>

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

### <span data-ttu-id="9bcaf-116">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="9bcaf-116">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="9bcaf-117">Сохранить хотя бы один вариант резервного копирования</span><span class="sxs-lookup"><span data-stu-id="9bcaf-117">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="9bcaf-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9bcaf-118">-Name</span></span>
<span data-ttu-id="9bcaf-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="9bcaf-119">WebApp Name</span></span>

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

### <span data-ttu-id="9bcaf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bcaf-120">-ResourceGroupName</span></span>
<span data-ttu-id="9bcaf-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9bcaf-121">Resource Group Name</span></span>

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

### <span data-ttu-id="9bcaf-122">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="9bcaf-122">-RetentionPeriodInDays</span></span>
<span data-ttu-id="9bcaf-123">Срок хранения в днях</span><span class="sxs-lookup"><span data-stu-id="9bcaf-123">Retention Period In Days</span></span>

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

### <span data-ttu-id="9bcaf-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="9bcaf-124">-Slot</span></span>
<span data-ttu-id="9bcaf-125">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="9bcaf-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9bcaf-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9bcaf-126">-StartTime</span></span>
<span data-ttu-id="9bcaf-127">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="9bcaf-127">StartTime in UTC</span></span>

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

### <span data-ttu-id="9bcaf-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="9bcaf-128">-StorageAccountUrl</span></span>
<span data-ttu-id="9bcaf-129">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9bcaf-129">Storage Account Url</span></span>

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

### <span data-ttu-id="9bcaf-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9bcaf-130">-WebApp</span></span>
<span data-ttu-id="9bcaf-131">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="9bcaf-131">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bcaf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bcaf-132">-DefaultProfile</span></span>
<span data-ttu-id="9bcaf-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bcaf-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bcaf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bcaf-134">CommonParameters</span></span>
<span data-ttu-id="9bcaf-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bcaf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bcaf-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bcaf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bcaf-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bcaf-137">INPUTS</span></span>

### <span data-ttu-id="9bcaf-138">Семейств</span><span class="sxs-lookup"><span data-stu-id="9bcaf-138">Site</span></span>
<span data-ttu-id="9bcaf-139">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9bcaf-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9bcaf-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bcaf-140">OUTPUTS</span></span>

### <span data-ttu-id="9bcaf-141">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bcaf-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="9bcaf-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bcaf-142">NOTES</span></span>

## <span data-ttu-id="9bcaf-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bcaf-143">RELATED LINKS</span></span>

[<span data-ttu-id="9bcaf-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="9bcaf-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


