---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 97373d35cee4efb80ca2953c0085fe6b153ea138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906249"
---
# <span data-ttu-id="da92c-101">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="da92c-101">Get-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="da92c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da92c-102">SYNOPSIS</span></span>
<span data-ttu-id="da92c-103">Возвращает политику географического резервного копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="da92c-103">Gets a database geo backup policy.</span></span>

## <span data-ttu-id="da92c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da92c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da92c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da92c-105">DESCRIPTION</span></span>
<span data-ttu-id="da92c-106">Командлет **Get-AzSqlDatabaseGeoBackupPolicy** получает политику географического резервного копирования, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="da92c-106">The **Get-AzSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="da92c-107">Это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="da92c-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="da92c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da92c-108">EXAMPLES</span></span>

## <span data-ttu-id="da92c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da92c-109">PARAMETERS</span></span>

### <span data-ttu-id="da92c-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da92c-110">-DatabaseName</span></span>
<span data-ttu-id="da92c-111">Указывает имя базы данных, для которой этот командлет получает политику географического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="da92c-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="da92c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da92c-112">-DefaultProfile</span></span>
<span data-ttu-id="da92c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="da92c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da92c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da92c-114">-ResourceGroupName</span></span>
<span data-ttu-id="da92c-115">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="da92c-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="da92c-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="da92c-116">-ServerName</span></span>
<span data-ttu-id="da92c-117">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="da92c-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="da92c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da92c-118">CommonParameters</span></span>
<span data-ttu-id="da92c-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da92c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da92c-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da92c-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da92c-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da92c-121">INPUTS</span></span>

### <span data-ttu-id="da92c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="da92c-122">System.String</span></span>

## <span data-ttu-id="da92c-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da92c-123">OUTPUTS</span></span>

### <span data-ttu-id="da92c-124">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="da92c-124">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="da92c-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="da92c-125">NOTES</span></span>

## <span data-ttu-id="da92c-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da92c-126">RELATED LINKS</span></span>

[<span data-ttu-id="da92c-127">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="da92c-127">Set-AzSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="da92c-128">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="da92c-128">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
