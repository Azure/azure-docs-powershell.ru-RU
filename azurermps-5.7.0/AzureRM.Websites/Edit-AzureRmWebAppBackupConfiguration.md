---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 9c23484fa5f8b45548985645db45872fcc63f66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567356"
---
# <span data-ttu-id="f717b-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f717b-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f717b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f717b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f717b-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f717b-103">SYNTAX</span></span>

### <span data-ttu-id="f717b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f717b-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="f717b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f717b-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="f717b-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f717b-106">DESCRIPTION</span></span>
<span data-ttu-id="f717b-107">Командлет **Edit-AzureRmWebAppBackupConfiguration** редактирует текущую резервную копию конфигурации для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f717b-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="f717b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f717b-108">EXAMPLES</span></span>

## <span data-ttu-id="f717b-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f717b-109">PARAMETERS</span></span>

### <span data-ttu-id="f717b-110">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="f717b-110">-Databases</span></span>
<span data-ttu-id="f717b-111">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="f717b-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="f717b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f717b-112">-DefaultProfile</span></span>
<span data-ttu-id="f717b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f717b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f717b-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="f717b-114">-FrequencyInterval</span></span>
<span data-ttu-id="f717b-115">Интервал частот</span><span class="sxs-lookup"><span data-stu-id="f717b-115">Frequency Interval</span></span>

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

### <span data-ttu-id="f717b-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="f717b-116">-FrequencyUnit</span></span>
<span data-ttu-id="f717b-117">Частотный блок</span><span class="sxs-lookup"><span data-stu-id="f717b-117">Frequency Unit</span></span>

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

### <span data-ttu-id="f717b-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="f717b-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="f717b-119">Сохранить хотя бы один вариант резервного копирования</span><span class="sxs-lookup"><span data-stu-id="f717b-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="f717b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f717b-120">-Name</span></span>
<span data-ttu-id="f717b-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="f717b-121">WebApp Name</span></span>

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

### <span data-ttu-id="f717b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f717b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f717b-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f717b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f717b-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f717b-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="f717b-125">Срок хранения в днях</span><span class="sxs-lookup"><span data-stu-id="f717b-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="f717b-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="f717b-126">-Slot</span></span>
<span data-ttu-id="f717b-127">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="f717b-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f717b-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f717b-128">-StartTime</span></span>
<span data-ttu-id="f717b-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="f717b-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="f717b-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f717b-130">-StorageAccountUrl</span></span>
<span data-ttu-id="f717b-131">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f717b-131">Storage Account Url</span></span>

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

### <span data-ttu-id="f717b-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f717b-132">-WebApp</span></span>
<span data-ttu-id="f717b-133">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="f717b-133">WebApp Object</span></span>

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

### <span data-ttu-id="f717b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f717b-134">CommonParameters</span></span>
<span data-ttu-id="f717b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f717b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f717b-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f717b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f717b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f717b-137">INPUTS</span></span>

### <span data-ttu-id="f717b-138">Семейств</span><span class="sxs-lookup"><span data-stu-id="f717b-138">Site</span></span>
<span data-ttu-id="f717b-139">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f717b-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f717b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f717b-140">OUTPUTS</span></span>

### <span data-ttu-id="f717b-141">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f717b-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="f717b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f717b-142">NOTES</span></span>

## <span data-ttu-id="f717b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f717b-143">RELATED LINKS</span></span>

[<span data-ttu-id="f717b-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f717b-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


