---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: 07cf4daffeaf00c516bc5b179e5f4a2133a2c4ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557679"
---
# <span data-ttu-id="44d71-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="44d71-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="44d71-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44d71-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44d71-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44d71-103">SYNTAX</span></span>

### <span data-ttu-id="44d71-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="44d71-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="44d71-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="44d71-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="44d71-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44d71-106">DESCRIPTION</span></span>
<span data-ttu-id="44d71-107">Командлет **RESTORE-AzureRmWebAppBackup** восстанавливает резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="44d71-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="44d71-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44d71-108">EXAMPLES</span></span>

### <span data-ttu-id="44d71-109">1:</span><span class="sxs-lookup"><span data-stu-id="44d71-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="44d71-110">Восстанавливает резервную копию указанного ContosoWebApp приложения, который находится в группе ресурсов по умолчанию — Web-WestUS in BLOB "myBlob", расположенной в https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="44d71-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="44d71-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44d71-111">PARAMETERS</span></span>

### <span data-ttu-id="44d71-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="44d71-112">-BlobName</span></span>
<span data-ttu-id="44d71-113">Имя BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="44d71-113">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d71-114">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="44d71-114">-Databases</span></span>
<span data-ttu-id="44d71-115">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="44d71-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d71-116">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="44d71-116">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="44d71-117">Параметр "игнорировать конфликтующие HostName"</span><span class="sxs-lookup"><span data-stu-id="44d71-117">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d71-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44d71-118">-Name</span></span>
<span data-ttu-id="44d71-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="44d71-119">WebApp Name</span></span>

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

### <span data-ttu-id="44d71-120">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="44d71-120">-Overwrite</span></span>
<span data-ttu-id="44d71-121">Параметр перезаписи</span><span class="sxs-lookup"><span data-stu-id="44d71-121">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d71-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d71-122">-ResourceGroupName</span></span>
<span data-ttu-id="44d71-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="44d71-123">Resource Group Name</span></span>

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

### <span data-ttu-id="44d71-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="44d71-124">-Slot</span></span>
<span data-ttu-id="44d71-125">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="44d71-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="44d71-126">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="44d71-126">-StorageAccountUrl</span></span>
<span data-ttu-id="44d71-127">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="44d71-127">Storage Account Url</span></span>

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

### <span data-ttu-id="44d71-128">-WebApp</span><span class="sxs-lookup"><span data-stu-id="44d71-128">-WebApp</span></span>
<span data-ttu-id="44d71-129">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="44d71-129">WebApp Object</span></span>

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

### <span data-ttu-id="44d71-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d71-130">-DefaultProfile</span></span>
<span data-ttu-id="44d71-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44d71-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44d71-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d71-132">CommonParameters</span></span>
<span data-ttu-id="44d71-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44d71-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d71-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d71-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d71-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44d71-135">INPUTS</span></span>

### <span data-ttu-id="44d71-136">Семейств</span><span class="sxs-lookup"><span data-stu-id="44d71-136">Site</span></span>
<span data-ttu-id="44d71-137">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="44d71-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="44d71-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44d71-138">OUTPUTS</span></span>

## <span data-ttu-id="44d71-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="44d71-139">NOTES</span></span>

## <span data-ttu-id="44d71-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44d71-140">RELATED LINKS</span></span>

