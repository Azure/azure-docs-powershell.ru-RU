---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 480532e2fffcc2b03a57c7d0a63cc2737844f652
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065203"
---
# <span data-ttu-id="b3dec-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="b3dec-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="b3dec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3dec-102">SYNOPSIS</span></span>

## <span data-ttu-id="b3dec-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3dec-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3dec-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3dec-104">DESCRIPTION</span></span>
<span data-ttu-id="b3dec-105">Командлет **New-AzWebAppDatabaseBackupSetting** создает новый параметр резервного копирования веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b3dec-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="b3dec-106">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3dec-106">EXAMPLES</span></span>

### <span data-ttu-id="b3dec-107">1:</span><span class="sxs-lookup"><span data-stu-id="b3dec-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="b3dec-108">Создает параметр резервного копирования базы данных (строка подключения) типа SqlAzure для указанного приложения ContosoWebApp, которое находится в группе ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b3dec-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b3dec-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3dec-109">PARAMETERS</span></span>

### <span data-ttu-id="b3dec-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b3dec-110">-ConnectionString</span></span>
<span data-ttu-id="b3dec-111">Строка подключения</span><span class="sxs-lookup"><span data-stu-id="b3dec-111">Connection String</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3dec-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="b3dec-112">-ConnectionStringName</span></span>
<span data-ttu-id="b3dec-113">Имя строки соединения</span><span class="sxs-lookup"><span data-stu-id="b3dec-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3dec-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="b3dec-114">-DatabaseType</span></span>
<span data-ttu-id="b3dec-115">Тип базы данных (например, "SqlAzure" или "MySql")</span><span class="sxs-lookup"><span data-stu-id="b3dec-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3dec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3dec-116">-DefaultProfile</span></span>
<span data-ttu-id="b3dec-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3dec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3dec-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3dec-118">-Name</span></span>
<span data-ttu-id="b3dec-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="b3dec-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3dec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3dec-120">CommonParameters</span></span>
<span data-ttu-id="b3dec-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3dec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3dec-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3dec-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3dec-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3dec-123">INPUTS</span></span>

### <span data-ttu-id="b3dec-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b3dec-124">System.String</span></span>

## <span data-ttu-id="b3dec-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3dec-125">OUTPUTS</span></span>

### <span data-ttu-id="b3dec-126">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="b3dec-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="b3dec-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3dec-127">NOTES</span></span>

## <span data-ttu-id="b3dec-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3dec-128">RELATED LINKS</span></span>
