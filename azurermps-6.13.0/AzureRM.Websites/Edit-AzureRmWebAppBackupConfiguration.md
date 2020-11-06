---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: a7a66197752e7dd9ec58e7eeca921af277687ed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558135"
---
# <span data-ttu-id="faf43-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf43-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="faf43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="faf43-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf43-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="faf43-103">SYNTAX</span></span>

### <span data-ttu-id="faf43-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="faf43-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="faf43-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="faf43-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="faf43-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="faf43-106">DESCRIPTION</span></span>
<span data-ttu-id="faf43-107">Командлет **Edit-AzureRmWebAppBackupConfiguration** редактирует текущую резервную копию конфигурации для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="faf43-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="faf43-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="faf43-108">EXAMPLES</span></span>

## <span data-ttu-id="faf43-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="faf43-109">PARAMETERS</span></span>

### <span data-ttu-id="faf43-110">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="faf43-110">-Databases</span></span>
<span data-ttu-id="faf43-111">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="faf43-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="faf43-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf43-112">-DefaultProfile</span></span>
<span data-ttu-id="faf43-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="faf43-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf43-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="faf43-114">-FrequencyInterval</span></span>
<span data-ttu-id="faf43-115">Интервал частот</span><span class="sxs-lookup"><span data-stu-id="faf43-115">Frequency Interval</span></span>

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

### <span data-ttu-id="faf43-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="faf43-116">-FrequencyUnit</span></span>
<span data-ttu-id="faf43-117">Частотный блок</span><span class="sxs-lookup"><span data-stu-id="faf43-117">Frequency Unit</span></span>

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

### <span data-ttu-id="faf43-118">-KeepAtLeastOneBackup</span><span class="sxs-lookup"><span data-stu-id="faf43-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="faf43-119">Сохранить хотя бы один вариант резервного копирования</span><span class="sxs-lookup"><span data-stu-id="faf43-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="faf43-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="faf43-120">-Name</span></span>
<span data-ttu-id="faf43-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="faf43-121">WebApp Name</span></span>

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

### <span data-ttu-id="faf43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf43-122">-ResourceGroupName</span></span>
<span data-ttu-id="faf43-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="faf43-123">Resource Group Name</span></span>

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

### <span data-ttu-id="faf43-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="faf43-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="faf43-125">Срок хранения в днях</span><span class="sxs-lookup"><span data-stu-id="faf43-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="faf43-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="faf43-126">-Slot</span></span>
<span data-ttu-id="faf43-127">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="faf43-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="faf43-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="faf43-128">-StartTime</span></span>
<span data-ttu-id="faf43-129">Время начала в формате UTC</span><span class="sxs-lookup"><span data-stu-id="faf43-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="faf43-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="faf43-130">-StorageAccountUrl</span></span>
<span data-ttu-id="faf43-131">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="faf43-131">Storage Account Url</span></span>

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

### <span data-ttu-id="faf43-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="faf43-132">-WebApp</span></span>
<span data-ttu-id="faf43-133">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="faf43-133">WebApp Object</span></span>

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

### <span data-ttu-id="faf43-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf43-134">CommonParameters</span></span>
<span data-ttu-id="faf43-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="faf43-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf43-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf43-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf43-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="faf43-137">INPUTS</span></span>

### <span data-ttu-id="faf43-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="faf43-138">System.Int32</span></span>

### <span data-ttu-id="faf43-139">System. String</span><span class="sxs-lookup"><span data-stu-id="faf43-139">System.String</span></span>

### <span data-ttu-id="faf43-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="faf43-140">System.DateTime</span></span>

### <span data-ttu-id="faf43-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="faf43-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="faf43-142">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="faf43-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="faf43-143">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="faf43-143">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="faf43-144">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="faf43-144">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="faf43-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="faf43-145">OUTPUTS</span></span>

### <span data-ttu-id="faf43-146">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf43-146">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="faf43-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="faf43-147">NOTES</span></span>

## <span data-ttu-id="faf43-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="faf43-148">RELATED LINKS</span></span>

[<span data-ttu-id="faf43-149">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="faf43-149">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


