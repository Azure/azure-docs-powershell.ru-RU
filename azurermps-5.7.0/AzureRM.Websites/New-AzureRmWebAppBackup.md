---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 7784ea832faef9f73b46b04d6ad36bebe0e2f36d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566869"
---
# <span data-ttu-id="3490d-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="3490d-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="3490d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3490d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3490d-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3490d-103">SYNTAX</span></span>

### <span data-ttu-id="3490d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="3490d-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="3490d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="3490d-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="3490d-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3490d-106">DESCRIPTION</span></span>
<span data-ttu-id="3490d-107">Командлет **New-AzureRmWebAppBackup** создает резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3490d-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="3490d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3490d-108">EXAMPLES</span></span>

### <span data-ttu-id="3490d-109">1:</span><span class="sxs-lookup"><span data-stu-id="3490d-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="3490d-110">Создание резервной копии указанного приложения ContosoWebApp, которое находится в группе ресурсов Default-Web-WestUS в https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="3490d-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="3490d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3490d-111">PARAMETERS</span></span>

### <span data-ttu-id="3490d-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="3490d-112">-BackupName</span></span>
<span data-ttu-id="3490d-113">Имя резервной копии</span><span class="sxs-lookup"><span data-stu-id="3490d-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3490d-114">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="3490d-114">-Databases</span></span>
<span data-ttu-id="3490d-115">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="3490d-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="3490d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3490d-116">-DefaultProfile</span></span>
<span data-ttu-id="3490d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3490d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3490d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3490d-118">-Name</span></span>
<span data-ttu-id="3490d-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="3490d-119">WebApp Name</span></span>

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

### <span data-ttu-id="3490d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3490d-120">-ResourceGroupName</span></span>
<span data-ttu-id="3490d-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3490d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="3490d-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="3490d-122">-Slot</span></span>
<span data-ttu-id="3490d-123">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="3490d-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3490d-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="3490d-124">-StorageAccountUrl</span></span>
<span data-ttu-id="3490d-125">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="3490d-125">Storage Account Url</span></span>

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

### <span data-ttu-id="3490d-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3490d-126">-WebApp</span></span>
<span data-ttu-id="3490d-127">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="3490d-127">WebApp Object</span></span>

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

### <span data-ttu-id="3490d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3490d-128">CommonParameters</span></span>
<span data-ttu-id="3490d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3490d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3490d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3490d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3490d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3490d-131">INPUTS</span></span>

### <span data-ttu-id="3490d-132">Семейств</span><span class="sxs-lookup"><span data-stu-id="3490d-132">Site</span></span>
<span data-ttu-id="3490d-133">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3490d-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3490d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3490d-134">OUTPUTS</span></span>

### <span data-ttu-id="3490d-135">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="3490d-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="3490d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3490d-136">NOTES</span></span>

## <span data-ttu-id="3490d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3490d-137">RELATED LINKS</span></span>

