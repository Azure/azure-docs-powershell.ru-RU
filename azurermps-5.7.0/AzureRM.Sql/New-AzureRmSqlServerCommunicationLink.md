---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 0492b81e5674ea08ad98dff1fca75335b1ec8fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566072"
---
# <span data-ttu-id="893b3-101">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="893b3-101">New-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="893b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="893b3-102">SYNOPSIS</span></span>
<span data-ttu-id="893b3-103">Создание коммуникационной ссылки для транзакций эластичной базы данных между двумя серверами баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="893b3-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="893b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="893b3-104">SYNTAX</span></span>

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="893b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="893b3-105">DESCRIPTION</span></span>
<span data-ttu-id="893b3-106">Командлет **New-AzureRmSqlServerCommunicationLink** создает канал связи для транзакций эластичных баз данных между двумя логическими серверами в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="893b3-106">The **New-AzureRmSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="893b3-107">Транзакции эластичных баз данных могут охватывать базы данных на любом из подключенных серверов.</span><span class="sxs-lookup"><span data-stu-id="893b3-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="893b3-108">Вы можете создать несколько ссылок на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="893b3-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="893b3-109">Таким образом, транзакции эластичной базы данных могут занимать больше всего серверов.</span><span class="sxs-lookup"><span data-stu-id="893b3-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="893b3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="893b3-110">EXAMPLES</span></span>

### <span data-ttu-id="893b3-111">Пример 1: создание коммуникационной ссылки</span><span class="sxs-lookup"><span data-stu-id="893b3-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="893b3-112">Эта команда создает ссылку с именем Link01 между ContosoServer17 и ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="893b3-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="893b3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="893b3-113">PARAMETERS</span></span>

### <span data-ttu-id="893b3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="893b3-114">-AsJob</span></span>
<span data-ttu-id="893b3-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="893b3-115">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893b3-116">-DefaultProfile</span></span>
<span data-ttu-id="893b3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="893b3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="893b3-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="893b3-118">-LinkName</span></span>
<span data-ttu-id="893b3-119">Указывает имя серверной ссылки, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="893b3-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893b3-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="893b3-120">-PartnerServer</span></span>
<span data-ttu-id="893b3-121">Указывает имя другого сервера, принимающего участие в этой коммуникационной ссылке.</span><span class="sxs-lookup"><span data-stu-id="893b3-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="893b3-123">Указывает имя группы ресурсов, к которой принадлежит сервер, указанный в параметре *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="893b3-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="893b3-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="893b3-124">-ServerName</span></span>
<span data-ttu-id="893b3-125">Указывает имя сервера, на котором этот командлет настраивает канал связи.</span><span class="sxs-lookup"><span data-stu-id="893b3-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="893b3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="893b3-126">-Confirm</span></span>
<span data-ttu-id="893b3-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="893b3-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893b3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="893b3-128">-WhatIf</span></span>
<span data-ttu-id="893b3-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="893b3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="893b3-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="893b3-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893b3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893b3-131">CommonParameters</span></span>
<span data-ttu-id="893b3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="893b3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893b3-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893b3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893b3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="893b3-134">INPUTS</span></span>

### <span data-ttu-id="893b3-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="893b3-135">None</span></span>
<span data-ttu-id="893b3-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="893b3-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="893b3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="893b3-137">OUTPUTS</span></span>

### <span data-ttu-id="893b3-138">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="893b3-138">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="893b3-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="893b3-139">NOTES</span></span>
* <span data-ttu-id="893b3-140">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="893b3-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="893b3-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="893b3-141">RELATED LINKS</span></span>

[<span data-ttu-id="893b3-142">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="893b3-142">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="893b3-143">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="893b3-143">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="893b3-144">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="893b3-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
