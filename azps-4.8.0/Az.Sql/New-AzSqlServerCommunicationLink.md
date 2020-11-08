---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078639"
---
# <span data-ttu-id="76d4c-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="76d4c-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="76d4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="76d4c-103">Создание коммуникационной ссылки для транзакций эластичной базы данных между двумя серверами баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="76d4c-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="76d4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76d4c-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76d4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="76d4c-106">Командлет **New-AzSqlServerCommunicationLink** создает канал связи для транзакций эластичных баз данных между двумя логическими серверами в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="76d4c-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="76d4c-107">Транзакции эластичных баз данных могут охватывать базы данных на любом из подключенных серверов.</span><span class="sxs-lookup"><span data-stu-id="76d4c-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="76d4c-108">Вы можете создать несколько ссылок на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="76d4c-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="76d4c-109">Таким образом, транзакции эластичной базы данных могут занимать больше всего серверов.</span><span class="sxs-lookup"><span data-stu-id="76d4c-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="76d4c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76d4c-110">EXAMPLES</span></span>

### <span data-ttu-id="76d4c-111">Пример 1: создание коммуникационной ссылки</span><span class="sxs-lookup"><span data-stu-id="76d4c-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="76d4c-112">Эта команда создает ссылку с именем Link01 между ContosoServer17 и ContosoServer02.</span><span class="sxs-lookup"><span data-stu-id="76d4c-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="76d4c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76d4c-113">PARAMETERS</span></span>

### <span data-ttu-id="76d4c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76d4c-114">-AsJob</span></span>
<span data-ttu-id="76d4c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="76d4c-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d4c-116">-DefaultProfile</span></span>
<span data-ttu-id="76d4c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="76d4c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76d4c-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="76d4c-118">-LinkName</span></span>
<span data-ttu-id="76d4c-119">Указывает имя серверной ссылки, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="76d4c-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d4c-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="76d4c-120">-PartnerServer</span></span>
<span data-ttu-id="76d4c-121">Указывает имя другого сервера, принимающего участие в этой коммуникационной ссылке.</span><span class="sxs-lookup"><span data-stu-id="76d4c-121">Specifies the name of the other server that takes part in this communication link.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="76d4c-123">Указывает имя группы ресурсов, к которой принадлежит сервер, указанный в параметре *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="76d4c-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="76d4c-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="76d4c-124">-ServerName</span></span>
<span data-ttu-id="76d4c-125">Указывает имя сервера, на котором этот командлет настраивает канал связи.</span><span class="sxs-lookup"><span data-stu-id="76d4c-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="76d4c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76d4c-126">-Confirm</span></span>
<span data-ttu-id="76d4c-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76d4c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d4c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76d4c-128">-WhatIf</span></span>
<span data-ttu-id="76d4c-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76d4c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76d4c-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76d4c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d4c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d4c-131">CommonParameters</span></span>
<span data-ttu-id="76d4c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76d4c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d4c-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76d4c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d4c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76d4c-134">INPUTS</span></span>

### <span data-ttu-id="76d4c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="76d4c-135">System.String</span></span>

## <span data-ttu-id="76d4c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76d4c-136">OUTPUTS</span></span>

### <span data-ttu-id="76d4c-137">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="76d4c-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="76d4c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="76d4c-138">NOTES</span></span>
* <span data-ttu-id="76d4c-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="76d4c-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="76d4c-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76d4c-140">RELATED LINKS</span></span>

[<span data-ttu-id="76d4c-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="76d4c-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="76d4c-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="76d4c-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="76d4c-143">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="76d4c-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)