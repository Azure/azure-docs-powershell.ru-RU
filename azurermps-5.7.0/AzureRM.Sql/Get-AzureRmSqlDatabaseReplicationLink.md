---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseReplicationLink.md
ms.openlocfilehash: 982a903d702f4143d9eb11e99fa15afc64a040e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732010"
---
# <span data-ttu-id="0ea22-101">Get-AzureRmSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="0ea22-101">Get-AzureRmSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="0ea22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ea22-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea22-103">Получает ссылки георепликации между базой данных Azure SQL и группой ресурсов или SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0ea22-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ea22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ea22-104">SYNTAX</span></span>

### <span data-ttu-id="0ea22-105">ByDatabaseName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ea22-105">ByDatabaseName (Default)</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ea22-106">ByPartnerServerName</span><span class="sxs-lookup"><span data-stu-id="0ea22-106">ByPartnerServerName</span></span>
```
Get-AzureRmSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ea22-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ea22-107">DESCRIPTION</span></span>
<span data-ttu-id="0ea22-108">Командлет **Get-AzureRMSqlDatabaseReplicationLink** заменяет командлет **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="0ea22-108">The **Get-AzureRMSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="0ea22-109">Она получает все ссылки георепликации между указанной базой данных Azure SQL и группой ресурсов или сервером AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="0ea22-109">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="0ea22-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ea22-110">EXAMPLES</span></span>

## <span data-ttu-id="0ea22-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ea22-111">PARAMETERS</span></span>

### <span data-ttu-id="0ea22-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0ea22-112">-DatabaseName</span></span>
<span data-ttu-id="0ea22-113">Указывает имя базы данных SQL, для которой требуется получить ссылки.</span><span class="sxs-lookup"><span data-stu-id="0ea22-113">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="0ea22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea22-114">-DefaultProfile</span></span>
<span data-ttu-id="0ea22-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0ea22-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ea22-116">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea22-116">-PartnerResourceGroupName</span></span>
<span data-ttu-id="0ea22-117">Указывает имя группы ресурсов, которой назначен партнер.</span><span class="sxs-lookup"><span data-stu-id="0ea22-117">Specifies the name of the resource group to which the partner is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ea22-118">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="0ea22-118">-PartnerServerName</span></span>
<span data-ttu-id="0ea22-119">Указывает имя сервера Azure SQL Server для партнера.</span><span class="sxs-lookup"><span data-stu-id="0ea22-119">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: String
Parameter Sets: ByPartnerServerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea22-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea22-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ea22-121">Указывает имя группы ресурсов Azure для базы данных, для которой требуется получить ссылки.</span><span class="sxs-lookup"><span data-stu-id="0ea22-121">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="0ea22-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0ea22-122">-ServerName</span></span>
<span data-ttu-id="0ea22-123">Указывает имя сервера SQL Server для базы данных, для которого требуется получить ссылки.</span><span class="sxs-lookup"><span data-stu-id="0ea22-123">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="0ea22-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ea22-124">-Confirm</span></span>
<span data-ttu-id="0ea22-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ea22-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea22-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea22-126">-WhatIf</span></span>
<span data-ttu-id="0ea22-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ea22-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ea22-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ea22-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ea22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea22-129">CommonParameters</span></span>
<span data-ttu-id="0ea22-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ea22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea22-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ea22-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea22-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ea22-132">INPUTS</span></span>

###  
<span data-ttu-id="0ea22-133">Этот командлет принимает экземпляры объекта **ReplicationLink** или **базы** данных для базы данных PRIMARY или Secondary.</span><span class="sxs-lookup"><span data-stu-id="0ea22-133">This cmdlet accepts instances of the **ReplicationLink** or the **Database** object for the primary or secondary database.</span></span>

## <span data-ttu-id="0ea22-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ea22-134">OUTPUTS</span></span>

###  
<span data-ttu-id="0ea22-135">Этот командлет возвращает объект **ReplicationLink** .</span><span class="sxs-lookup"><span data-stu-id="0ea22-135">This cmdlet returns a **ReplicationLink** object.</span></span>

## <span data-ttu-id="0ea22-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ea22-136">NOTES</span></span>

## <span data-ttu-id="0ea22-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ea22-137">RELATED LINKS</span></span>

[<span data-ttu-id="0ea22-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="0ea22-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
