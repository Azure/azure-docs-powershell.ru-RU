---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 7245697cab6184aa5fc2f7c292875f96cf3de3fb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913711"
---
# <span data-ttu-id="6b6df-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6b6df-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="6b6df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b6df-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b6df-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b6df-103">SYNTAX</span></span>

### <span data-ttu-id="6b6df-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6b6df-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="6b6df-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6b6df-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="6b6df-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b6df-106">DESCRIPTION</span></span>
<span data-ttu-id="6b6df-107">Командлет **New-AzureRmWebAppBackup** создает резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6df-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="6b6df-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b6df-108">EXAMPLES</span></span>

### <span data-ttu-id="6b6df-109">1:</span><span class="sxs-lookup"><span data-stu-id="6b6df-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="6b6df-110">Создание резервной копии указанного приложения ContosoWebApp, которое находится в группе ресурсов Default-Web-WestUS в https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="6b6df-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="6b6df-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b6df-111">PARAMETERS</span></span>

### <span data-ttu-id="6b6df-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="6b6df-112">-BackupName</span></span>
<span data-ttu-id="6b6df-113">Имя резервной копии</span><span class="sxs-lookup"><span data-stu-id="6b6df-113">Backup Name</span></span>

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

### <span data-ttu-id="6b6df-114">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="6b6df-114">-Databases</span></span>
<span data-ttu-id="6b6df-115">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="6b6df-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="6b6df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b6df-116">-DefaultProfile</span></span>
<span data-ttu-id="6b6df-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b6df-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b6df-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b6df-118">-Name</span></span>
<span data-ttu-id="6b6df-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="6b6df-119">WebApp Name</span></span>

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

### <span data-ttu-id="6b6df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b6df-120">-ResourceGroupName</span></span>
<span data-ttu-id="6b6df-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6b6df-121">Resource Group Name</span></span>

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

### <span data-ttu-id="6b6df-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="6b6df-122">-Slot</span></span>
<span data-ttu-id="6b6df-123">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="6b6df-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="6b6df-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="6b6df-124">-StorageAccountUrl</span></span>
<span data-ttu-id="6b6df-125">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6b6df-125">Storage Account Url</span></span>

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

### <span data-ttu-id="6b6df-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6b6df-126">-WebApp</span></span>
<span data-ttu-id="6b6df-127">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="6b6df-127">WebApp Object</span></span>

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

### <span data-ttu-id="6b6df-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b6df-128">CommonParameters</span></span>
<span data-ttu-id="6b6df-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b6df-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b6df-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b6df-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b6df-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b6df-131">INPUTS</span></span>

### <span data-ttu-id="6b6df-132">Семейств</span><span class="sxs-lookup"><span data-stu-id="6b6df-132">Site</span></span>
<span data-ttu-id="6b6df-133">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6b6df-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6b6df-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b6df-134">OUTPUTS</span></span>

### <span data-ttu-id="6b6df-135">Microsoft. Azure. Commands. Apps. командлеты. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6b6df-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="6b6df-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b6df-136">NOTES</span></span>

## <span data-ttu-id="6b6df-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b6df-137">RELATED LINKS</span></span>

