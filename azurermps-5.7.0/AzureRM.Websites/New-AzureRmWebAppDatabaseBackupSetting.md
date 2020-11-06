---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7eea25d4b82dc8a424fea0cbd3e361014c77c396
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566865"
---
# <span data-ttu-id="24d21-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="24d21-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="24d21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24d21-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24d21-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24d21-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24d21-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24d21-104">DESCRIPTION</span></span>
<span data-ttu-id="24d21-105">Командлет **New-AzureRmWebAppDatabaseBackupSetting** создает новый параметр резервного копирования веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="24d21-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="24d21-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24d21-106">EXAMPLES</span></span>

### <span data-ttu-id="24d21-107">1:</span><span class="sxs-lookup"><span data-stu-id="24d21-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="24d21-108">Создает параметр резервного копирования базы данных (строка подключения) типа SqlAzure для указанного приложения ContosoWebApp, которое находится в группе ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="24d21-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="24d21-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24d21-109">PARAMETERS</span></span>

### <span data-ttu-id="24d21-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="24d21-110">-ConnectionString</span></span>
<span data-ttu-id="24d21-111">Строка подключения</span><span class="sxs-lookup"><span data-stu-id="24d21-111">Connection String</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d21-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="24d21-112">-ConnectionStringName</span></span>
<span data-ttu-id="24d21-113">Имя строки соединения</span><span class="sxs-lookup"><span data-stu-id="24d21-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d21-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="24d21-114">-DatabaseType</span></span>
<span data-ttu-id="24d21-115">Тип базы данных (например, "SqlAzure" или "MySql")</span><span class="sxs-lookup"><span data-stu-id="24d21-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d21-116">-DefaultProfile</span></span>
<span data-ttu-id="24d21-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24d21-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24d21-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24d21-118">-Name</span></span>
<span data-ttu-id="24d21-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="24d21-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d21-120">CommonParameters</span></span>
<span data-ttu-id="24d21-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24d21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d21-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d21-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d21-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24d21-123">INPUTS</span></span>

### <span data-ttu-id="24d21-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="24d21-124">None</span></span>
<span data-ttu-id="24d21-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="24d21-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24d21-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24d21-126">OUTPUTS</span></span>

### <span data-ttu-id="24d21-127">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="24d21-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="24d21-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="24d21-128">NOTES</span></span>

## <span data-ttu-id="24d21-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24d21-129">RELATED LINKS</span></span>

