---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: a7aadc195be162db5f612dae47451f0b118fce19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078699"
---
# <span data-ttu-id="9bf19-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9bf19-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="9bf19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bf19-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf19-103">Возвращает политику географического резервного копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="9bf19-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="9bf19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bf19-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf19-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bf19-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf19-106">Командлет **Get-AzSqlDatabaseGeoBackupPolicy** получает политику географического резервного копирования, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="9bf19-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="9bf19-107">Это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="9bf19-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="9bf19-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bf19-108">EXAMPLES</span></span>

### <span data-ttu-id="9bf19-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9bf19-109">Example 1</span></span>

<span data-ttu-id="9bf19-110">Возвращает политику географического резервного копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="9bf19-110">Gets a database geo backup policy.</span></span> <span data-ttu-id="9bf19-111">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="9bf19-111">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlDatabaseGeoBackupPolicy -DatabaseName db1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="9bf19-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bf19-112">PARAMETERS</span></span>

### <span data-ttu-id="9bf19-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9bf19-113">-DatabaseName</span></span>
<span data-ttu-id="9bf19-114">Указывает имя базы данных, для которой этот командлет получает политику географического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="9bf19-114">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="9bf19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf19-115">-DefaultProfile</span></span>
<span data-ttu-id="9bf19-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9bf19-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bf19-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf19-117">-ResourceGroupName</span></span>
<span data-ttu-id="9bf19-118">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="9bf19-118">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="9bf19-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9bf19-119">-ServerName</span></span>
<span data-ttu-id="9bf19-120">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="9bf19-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="9bf19-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf19-121">CommonParameters</span></span>
<span data-ttu-id="9bf19-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bf19-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf19-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bf19-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf19-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bf19-124">INPUTS</span></span>

### <span data-ttu-id="9bf19-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf19-125">System.String</span></span>

## <span data-ttu-id="9bf19-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bf19-126">OUTPUTS</span></span>

### <span data-ttu-id="9bf19-127">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="9bf19-127">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="9bf19-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bf19-128">NOTES</span></span>

## <span data-ttu-id="9bf19-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bf19-129">RELATED LINKS</span></span>

[<span data-ttu-id="9bf19-130">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="9bf19-130">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="9bf19-131">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9bf19-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)