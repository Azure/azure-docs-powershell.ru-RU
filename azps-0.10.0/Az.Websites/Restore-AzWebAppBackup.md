---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: f93a173e79cb34c5603ce58fc3e03c92869a5d01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910568"
---
# <span data-ttu-id="7049e-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="7049e-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="7049e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7049e-102">SYNOPSIS</span></span>

## <span data-ttu-id="7049e-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7049e-103">SYNTAX</span></span>

### <span data-ttu-id="7049e-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7049e-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="7049e-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7049e-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="7049e-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7049e-106">DESCRIPTION</span></span>
<span data-ttu-id="7049e-107">Командлет **RESTORE-AzWebAppBackup** восстанавливает резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="7049e-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="7049e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7049e-108">EXAMPLES</span></span>

### <span data-ttu-id="7049e-109">1:</span><span class="sxs-lookup"><span data-stu-id="7049e-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="7049e-110">Восстанавливает резервную копию указанного ContosoWebApp приложения, который находится в группе ресурсов по умолчанию — Web-WestUS in BLOB "myBlob", расположенной в https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="7049e-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="7049e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7049e-111">PARAMETERS</span></span>

### <span data-ttu-id="7049e-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7049e-112">-AppServicePlan</span></span>
<span data-ttu-id="7049e-113">Имя плана служб приложений для восстановленного приложения.</span><span class="sxs-lookup"><span data-stu-id="7049e-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="7049e-114">Если оставить это поле пустым, используется текущий план служб приложений приложения.</span><span class="sxs-lookup"><span data-stu-id="7049e-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7049e-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="7049e-115">-BlobName</span></span>
<span data-ttu-id="7049e-116">Имя BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="7049e-116">Blob Name</span></span>

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

### <span data-ttu-id="7049e-117">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="7049e-117">-Databases</span></span>
<span data-ttu-id="7049e-118">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="7049e-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="7049e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7049e-119">-DefaultProfile</span></span>
<span data-ttu-id="7049e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7049e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7049e-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="7049e-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="7049e-122">Параметр "игнорировать конфликтующие HostName"</span><span class="sxs-lookup"><span data-stu-id="7049e-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="7049e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7049e-123">-Name</span></span>
<span data-ttu-id="7049e-124">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="7049e-124">WebApp Name</span></span>

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

### <span data-ttu-id="7049e-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="7049e-125">-Overwrite</span></span>
<span data-ttu-id="7049e-126">Параметр перезаписи</span><span class="sxs-lookup"><span data-stu-id="7049e-126">Overwrite Option</span></span>

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

### <span data-ttu-id="7049e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7049e-127">-ResourceGroupName</span></span>
<span data-ttu-id="7049e-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7049e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="7049e-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="7049e-129">-Slot</span></span>
<span data-ttu-id="7049e-130">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="7049e-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7049e-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="7049e-131">-StorageAccountUrl</span></span>
<span data-ttu-id="7049e-132">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7049e-132">Storage Account Url</span></span>

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

### <span data-ttu-id="7049e-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7049e-133">-WebApp</span></span>
<span data-ttu-id="7049e-134">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="7049e-134">WebApp Object</span></span>

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

### <span data-ttu-id="7049e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7049e-135">CommonParameters</span></span>
<span data-ttu-id="7049e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7049e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7049e-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7049e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7049e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7049e-138">INPUTS</span></span>

### <span data-ttu-id="7049e-139">Семейств</span><span class="sxs-lookup"><span data-stu-id="7049e-139">Site</span></span>
<span data-ttu-id="7049e-140">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7049e-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7049e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7049e-141">OUTPUTS</span></span>

## <span data-ttu-id="7049e-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7049e-142">NOTES</span></span>

## <span data-ttu-id="7049e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7049e-143">RELATED LINKS</span></span>

