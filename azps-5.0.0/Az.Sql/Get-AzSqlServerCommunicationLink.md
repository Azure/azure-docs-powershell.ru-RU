---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246986"
---
# <span data-ttu-id="f188b-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f188b-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="f188b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f188b-102">SYNOPSIS</span></span>
<span data-ttu-id="f188b-103">Получает коммуникационные ссылки на транзакции эластичных баз данных между серверами баз данных.</span><span class="sxs-lookup"><span data-stu-id="f188b-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="f188b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f188b-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f188b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f188b-105">DESCRIPTION</span></span>
<span data-ttu-id="f188b-106">Командлет **Get-AzSqlServerCommunicationLink** получает коммуникационные ссылки "сервер-сервер" для транзакций эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f188b-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="f188b-107">Укажите имя коммуникационной ссылки на сервер, чтобы просмотреть свойства этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="f188b-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="f188b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f188b-108">EXAMPLES</span></span>

### <span data-ttu-id="f188b-109">Пример 1: получение всех коммуникационных ссылок на сервер</span><span class="sxs-lookup"><span data-stu-id="f188b-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="f188b-110">Эта команда получает все ссылки на связь между сервером для транзакций эластичных баз данных для сервера с именем ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="f188b-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="f188b-111">Пример 2: получение специальной коммуникационной ссылки для сервера</span><span class="sxs-lookup"><span data-stu-id="f188b-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="f188b-112">Эта команда получает связь между сервером и сервером с именем Link01.</span><span class="sxs-lookup"><span data-stu-id="f188b-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="f188b-113">Пример 3: получение всех коммуникационных ссылок на сервер с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="f188b-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="f188b-114">Эта команда получает все ссылки на связь между сервером для транзакций эластичных баз данных для сервера с именем ContosoServer17, который начинается со слова Link.</span><span class="sxs-lookup"><span data-stu-id="f188b-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="f188b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f188b-115">PARAMETERS</span></span>

### <span data-ttu-id="f188b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f188b-116">-DefaultProfile</span></span>
<span data-ttu-id="f188b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f188b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f188b-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="f188b-118">-LinkName</span></span>
<span data-ttu-id="f188b-119">Указывает имя серверной ссылки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f188b-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f188b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f188b-120">-ResourceGroupName</span></span>
<span data-ttu-id="f188b-121">Указывает имя группы ресурсов, к которой принадлежит сервер, указанный в параметре *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="f188b-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="f188b-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f188b-122">-ServerName</span></span>
<span data-ttu-id="f188b-123">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f188b-123">Specifies the name of a server.</span></span>
<span data-ttu-id="f188b-124">Этот сервер включает ссылку для связи, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f188b-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f188b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f188b-125">-Confirm</span></span>
<span data-ttu-id="f188b-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f188b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f188b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f188b-127">-WhatIf</span></span>
<span data-ttu-id="f188b-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f188b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f188b-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f188b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f188b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f188b-130">CommonParameters</span></span>
<span data-ttu-id="f188b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f188b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f188b-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f188b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f188b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f188b-133">INPUTS</span></span>

### <span data-ttu-id="f188b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f188b-134">System.String</span></span>

## <span data-ttu-id="f188b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f188b-135">OUTPUTS</span></span>

### <span data-ttu-id="f188b-136">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="f188b-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="f188b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f188b-137">NOTES</span></span>
* <span data-ttu-id="f188b-138">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="f188b-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="f188b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f188b-139">RELATED LINKS</span></span>

[<span data-ttu-id="f188b-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f188b-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="f188b-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f188b-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="f188b-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f188b-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
