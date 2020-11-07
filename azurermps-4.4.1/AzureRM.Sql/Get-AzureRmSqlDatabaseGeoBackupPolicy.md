---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: b8f7d04a709ebb14ed6a7a76cffab556c13d26ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734761"
---
# <span data-ttu-id="622b8-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="622b8-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="622b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="622b8-102">SYNOPSIS</span></span>
<span data-ttu-id="622b8-103">Возвращает политику географического резервного копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="622b8-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="622b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="622b8-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="622b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="622b8-105">DESCRIPTION</span></span>
<span data-ttu-id="622b8-106">Командлет **Get-AzureRmSqlDatabaseGeoBackupPolicy** получает политику географического резервного копирования, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="622b8-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="622b8-107">Это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="622b8-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="622b8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="622b8-108">EXAMPLES</span></span>

## <span data-ttu-id="622b8-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="622b8-109">PARAMETERS</span></span>

### <span data-ttu-id="622b8-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="622b8-110">-DatabaseName</span></span>
<span data-ttu-id="622b8-111">Указывает имя базы данных, для которой этот командлет получает политику географического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="622b8-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="622b8-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="622b8-112">-ResourceGroupName</span></span>
<span data-ttu-id="622b8-113">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="622b8-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="622b8-114">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="622b8-114">-ServerName</span></span>
<span data-ttu-id="622b8-115">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="622b8-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="622b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="622b8-116">-DefaultProfile</span></span>
<span data-ttu-id="622b8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="622b8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="622b8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="622b8-118">CommonParameters</span></span>
<span data-ttu-id="622b8-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="622b8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="622b8-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="622b8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="622b8-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="622b8-121">INPUTS</span></span>

## <span data-ttu-id="622b8-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="622b8-122">OUTPUTS</span></span>

## <span data-ttu-id="622b8-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="622b8-123">NOTES</span></span>

## <span data-ttu-id="622b8-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="622b8-124">RELATED LINKS</span></span>

[<span data-ttu-id="622b8-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="622b8-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="622b8-126">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="622b8-126">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
