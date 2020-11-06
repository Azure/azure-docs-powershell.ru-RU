---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567346"
---
# <span data-ttu-id="ebe96-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="ebe96-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="ebe96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebe96-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebe96-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebe96-103">SYNTAX</span></span>

### <span data-ttu-id="ebe96-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ebe96-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="ebe96-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ebe96-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="ebe96-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebe96-106">DESCRIPTION</span></span>
<span data-ttu-id="ebe96-107">Командлет **RESTORE-AzureRmWebAppBackup** восстанавливает резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe96-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="ebe96-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebe96-108">EXAMPLES</span></span>

### <span data-ttu-id="ebe96-109">1:</span><span class="sxs-lookup"><span data-stu-id="ebe96-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="ebe96-110">Восстанавливает резервную копию указанного ContosoWebApp приложения, который находится в группе ресурсов по умолчанию — Web-WestUS in BLOB "myBlob", расположенной в https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="ebe96-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="ebe96-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebe96-111">PARAMETERS</span></span>

### <span data-ttu-id="ebe96-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="ebe96-112">-BlobName</span></span>
<span data-ttu-id="ebe96-113">Имя BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="ebe96-113">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe96-114">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="ebe96-114">-Databases</span></span>
<span data-ttu-id="ebe96-115">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ebe96-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe96-116">-DefaultProfile</span></span>
<span data-ttu-id="ebe96-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe96-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebe96-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="ebe96-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="ebe96-119">Параметр "игнорировать конфликтующие HostName"</span><span class="sxs-lookup"><span data-stu-id="ebe96-119">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="ebe96-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebe96-120">-Name</span></span>
<span data-ttu-id="ebe96-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ebe96-121">WebApp Name</span></span>

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

### <span data-ttu-id="ebe96-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ebe96-122">-Overwrite</span></span>
<span data-ttu-id="ebe96-123">Параметр перезаписи</span><span class="sxs-lookup"><span data-stu-id="ebe96-123">Overwrite Option</span></span>

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

### <span data-ttu-id="ebe96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe96-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebe96-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ebe96-125">Resource Group Name</span></span>

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

### <span data-ttu-id="ebe96-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="ebe96-126">-Slot</span></span>
<span data-ttu-id="ebe96-127">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="ebe96-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ebe96-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ebe96-128">-StorageAccountUrl</span></span>
<span data-ttu-id="ebe96-129">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ebe96-129">Storage Account Url</span></span>

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

### <span data-ttu-id="ebe96-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ebe96-130">-WebApp</span></span>
<span data-ttu-id="ebe96-131">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="ebe96-131">WebApp Object</span></span>

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

### <span data-ttu-id="ebe96-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe96-132">CommonParameters</span></span>
<span data-ttu-id="ebe96-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebe96-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe96-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebe96-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe96-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebe96-135">INPUTS</span></span>

### <span data-ttu-id="ebe96-136">Семейств</span><span class="sxs-lookup"><span data-stu-id="ebe96-136">Site</span></span>
<span data-ttu-id="ebe96-137">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ebe96-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ebe96-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebe96-138">OUTPUTS</span></span>

## <span data-ttu-id="ebe96-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebe96-139">NOTES</span></span>

## <span data-ttu-id="ebe96-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebe96-140">RELATED LINKS</span></span>

