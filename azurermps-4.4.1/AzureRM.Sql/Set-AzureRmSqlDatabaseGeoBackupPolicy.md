---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 2cf85aac2d301653787bdf227db1cd187a887986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562020"
---
# <span data-ttu-id="bbabf-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bbabf-101">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="bbabf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbabf-102">SYNOPSIS</span></span>
<span data-ttu-id="bbabf-103">Задает политику географического резервного копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="bbabf-103">Sets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbabf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbabf-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbabf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbabf-105">DESCRIPTION</span></span>
<span data-ttu-id="bbabf-106">Командлет **Set-AzureRmSqlDatabaseGeoBackupPolicy** задает политику географического резервного копирования, зарегистрированную в базе данных.</span><span class="sxs-lookup"><span data-stu-id="bbabf-106">The **Set-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="bbabf-107">Это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="bbabf-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="bbabf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbabf-108">EXAMPLES</span></span>

## <span data-ttu-id="bbabf-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbabf-109">PARAMETERS</span></span>

### <span data-ttu-id="bbabf-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bbabf-110">-DatabaseName</span></span>
<span data-ttu-id="bbabf-111">Указывает имя базы данных, для которой этот командлет задает политику географического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bbabf-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="bbabf-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbabf-112">-ResourceGroupName</span></span>
<span data-ttu-id="bbabf-113">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="bbabf-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="bbabf-114">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bbabf-114">-ServerName</span></span>
<span data-ttu-id="bbabf-115">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="bbabf-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="bbabf-116">-State</span><span class="sxs-lookup"><span data-stu-id="bbabf-116">-State</span></span>
<span data-ttu-id="bbabf-117">Задает состояние политики географического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="bbabf-117">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="bbabf-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bbabf-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bbabf-119">Включаем</span><span class="sxs-lookup"><span data-stu-id="bbabf-119">Enabled</span></span> 
- <span data-ttu-id="bbabf-120">Отключает</span><span class="sxs-lookup"><span data-stu-id="bbabf-120">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbabf-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbabf-121">-Confirm</span></span>
<span data-ttu-id="bbabf-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bbabf-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbabf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbabf-123">-WhatIf</span></span>
<span data-ttu-id="bbabf-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bbabf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbabf-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbabf-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbabf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbabf-126">-DefaultProfile</span></span>
<span data-ttu-id="bbabf-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbabf-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbabf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbabf-128">CommonParameters</span></span>
<span data-ttu-id="bbabf-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbabf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbabf-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbabf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbabf-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbabf-131">INPUTS</span></span>

## <span data-ttu-id="bbabf-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbabf-132">OUTPUTS</span></span>

## <span data-ttu-id="bbabf-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbabf-133">NOTES</span></span>

## <span data-ttu-id="bbabf-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbabf-134">RELATED LINKS</span></span>

[<span data-ttu-id="bbabf-135">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="bbabf-135">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="bbabf-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="bbabf-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

