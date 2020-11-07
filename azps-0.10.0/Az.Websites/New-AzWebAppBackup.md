---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: a01c49ac6591cfec7d8087d664ba61ddd825ac5e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910602"
---
# <span data-ttu-id="6dca5-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6dca5-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="6dca5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6dca5-102">SYNOPSIS</span></span>

## <span data-ttu-id="6dca5-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6dca5-103">SYNTAX</span></span>

### <span data-ttu-id="6dca5-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6dca5-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="6dca5-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6dca5-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="6dca5-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dca5-106">DESCRIPTION</span></span>
<span data-ttu-id="6dca5-107">Командлет **New-AzWebAppBackup** создает резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="6dca5-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="6dca5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6dca5-108">EXAMPLES</span></span>

### <span data-ttu-id="6dca5-109">1:</span><span class="sxs-lookup"><span data-stu-id="6dca5-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="6dca5-110">Создание резервной копии указанного приложения ContosoWebApp, которое находится в группе ресурсов Default-Web-WestUS в https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="6dca5-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="6dca5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6dca5-111">PARAMETERS</span></span>

### <span data-ttu-id="6dca5-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="6dca5-112">-BackupName</span></span>
<span data-ttu-id="6dca5-113">Имя резервной копии</span><span class="sxs-lookup"><span data-stu-id="6dca5-113">Backup Name</span></span>

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

### <span data-ttu-id="6dca5-114">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="6dca5-114">-Databases</span></span>
<span data-ttu-id="6dca5-115">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="6dca5-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="6dca5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dca5-116">-DefaultProfile</span></span>
<span data-ttu-id="6dca5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6dca5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dca5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6dca5-118">-Name</span></span>
<span data-ttu-id="6dca5-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="6dca5-119">WebApp Name</span></span>

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

### <span data-ttu-id="6dca5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dca5-120">-ResourceGroupName</span></span>
<span data-ttu-id="6dca5-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6dca5-121">Resource Group Name</span></span>

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

### <span data-ttu-id="6dca5-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="6dca5-122">-Slot</span></span>
<span data-ttu-id="6dca5-123">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="6dca5-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6dca5-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="6dca5-124">-StorageAccountUrl</span></span>
<span data-ttu-id="6dca5-125">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6dca5-125">Storage Account Url</span></span>

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

### <span data-ttu-id="6dca5-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6dca5-126">-WebApp</span></span>
<span data-ttu-id="6dca5-127">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="6dca5-127">WebApp Object</span></span>

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

### <span data-ttu-id="6dca5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dca5-128">CommonParameters</span></span>
<span data-ttu-id="6dca5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6dca5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dca5-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dca5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dca5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6dca5-131">INPUTS</span></span>

### <span data-ttu-id="6dca5-132">Семейств</span><span class="sxs-lookup"><span data-stu-id="6dca5-132">Site</span></span>
<span data-ttu-id="6dca5-133">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6dca5-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6dca5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dca5-134">OUTPUTS</span></span>

### <span data-ttu-id="6dca5-135">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6dca5-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="6dca5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6dca5-136">NOTES</span></span>

## <span data-ttu-id="6dca5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dca5-137">RELATED LINKS</span></span>

