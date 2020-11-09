---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318371"
---
# <span data-ttu-id="a4a5f-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="a4a5f-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="a4a5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a5f-103">Удаляет связь для транзакций эластичных баз данных между двумя серверами.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="a4a5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4a5f-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="a4a5f-106">Командлет **Remove-AzSqlServerCommunicationLink** удаляет связь "сервер-сервер" для транзакций эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="a4a5f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4a5f-107">EXAMPLES</span></span>

### <span data-ttu-id="a4a5f-108">Пример 1: удаление коммуникационной ссылки</span><span class="sxs-lookup"><span data-stu-id="a4a5f-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="a4a5f-109">Эта команда удаляет связь "сервер-сервер" с именем Link01 на ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="a4a5f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4a5f-110">PARAMETERS</span></span>

### <span data-ttu-id="a4a5f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a5f-111">-DefaultProfile</span></span>
<span data-ttu-id="a4a5f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a4a5f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4a5f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a4a5f-113">-Force</span></span>
<span data-ttu-id="a4a5f-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4a5f-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="a4a5f-115">-LinkName</span></span>
<span data-ttu-id="a4a5f-116">Указывает имя связи сервера, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a4a5f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a5f-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4a5f-118">Указывает имя группы ресурсов, к которой принадлежит сервер, указанный в параметре *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="a4a5f-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="a4a5f-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a4a5f-119">-ServerName</span></span>
<span data-ttu-id="a4a5f-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-120">Specifies the name of a server.</span></span>
<span data-ttu-id="a4a5f-121">Этот сервер включает ссылку для связи, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a4a5f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4a5f-122">-Confirm</span></span>
<span data-ttu-id="a4a5f-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4a5f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4a5f-124">-WhatIf</span></span>
<span data-ttu-id="a4a5f-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4a5f-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4a5f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a5f-127">CommonParameters</span></span>
<span data-ttu-id="a4a5f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4a5f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a5f-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4a5f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a5f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4a5f-130">INPUTS</span></span>

### <span data-ttu-id="a4a5f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a4a5f-131">System.String</span></span>

## <span data-ttu-id="a4a5f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4a5f-132">OUTPUTS</span></span>

### <span data-ttu-id="a4a5f-133">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="a4a5f-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="a4a5f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4a5f-134">NOTES</span></span>
* <span data-ttu-id="a4a5f-135">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="a4a5f-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="a4a5f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4a5f-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4a5f-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="a4a5f-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="a4a5f-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="a4a5f-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="a4a5f-139">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a4a5f-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)