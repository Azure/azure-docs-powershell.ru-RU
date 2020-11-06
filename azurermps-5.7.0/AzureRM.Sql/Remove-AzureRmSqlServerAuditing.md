---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 692D0B64-95EB-4D36-975F-65674B3B2F8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerAuditing.md
ms.openlocfilehash: bd5d8d2c63b10ecc4aaabd5e96ab1ce844602325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563272"
---
# <span data-ttu-id="37e7a-101">Remove-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="37e7a-101">Remove-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="37e7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="37e7a-103">Удаляет аудит сервера SQL Server.</span><span class="sxs-lookup"><span data-stu-id="37e7a-103">Removes the auditing of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37e7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37e7a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerAuditing [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e7a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="37e7a-106">Командлет **Remove-AzureRmSqlServerAuditing** удаляет аудит сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="37e7a-106">The **Remove-AzureRmSqlServerAuditing** cmdlet removes the auditing of an Azure SQL server.</span></span>
<span data-ttu-id="37e7a-107">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* и *ServerName* для идентификации сервера.</span><span class="sxs-lookup"><span data-stu-id="37e7a-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="37e7a-108">После запуска этого командлета аудит баз данных на сервере Azure SQL Server не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37e7a-108">After you run this cmdlet, auditing of the databases on the Azure SQL server is not performed.</span></span>
<span data-ttu-id="37e7a-109">Если команда пройдет успешно и вы задаете параметр *PassThru* , командлет возвращает объект, который описывает текущую политику аудита и идентификаторы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="37e7a-109">If the command succeeds, and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy and the Azure SQL server identifiers.</span></span>
<span data-ttu-id="37e7a-110">Идентификаторы сервера включают **ResourceGroupName** и **ServerName**.</span><span class="sxs-lookup"><span data-stu-id="37e7a-110">Server identifiers include the **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="37e7a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37e7a-111">EXAMPLES</span></span>

### <span data-ttu-id="37e7a-112">Пример 1: удаление аудита сервера Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="37e7a-112">Example 1: Remove the auditing of an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="37e7a-113">Эта команда удаляет аудит всех баз данных, расположенных в Server01, в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37e7a-113">This command removes the auditing of all the databases located on Server01 in resource group.</span></span>

## <span data-ttu-id="37e7a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37e7a-114">PARAMETERS</span></span>

### <span data-ttu-id="37e7a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e7a-115">-DefaultProfile</span></span>
<span data-ttu-id="37e7a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="37e7a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37e7a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37e7a-117">-PassThru</span></span>
<span data-ttu-id="37e7a-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="37e7a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="37e7a-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="37e7a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="37e7a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e7a-120">-ResourceGroupName</span></span>
<span data-ttu-id="37e7a-121">Указывает имя группы ресурсов, которой назначен Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="37e7a-121">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="37e7a-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="37e7a-122">-ServerName</span></span>
<span data-ttu-id="37e7a-123">Указывает имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="37e7a-123">Specifies the name of the Azure SQL server.</span></span>

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

### <span data-ttu-id="37e7a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37e7a-124">-Confirm</span></span>
<span data-ttu-id="37e7a-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="37e7a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e7a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e7a-126">-WhatIf</span></span>
<span data-ttu-id="37e7a-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="37e7a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e7a-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="37e7a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e7a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e7a-129">CommonParameters</span></span>
<span data-ttu-id="37e7a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37e7a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e7a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37e7a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e7a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37e7a-132">INPUTS</span></span>

### <span data-ttu-id="37e7a-133">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="37e7a-133">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="37e7a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37e7a-134">OUTPUTS</span></span>

### <span data-ttu-id="37e7a-135">Microsoft. Azure. Commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="37e7a-135">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="37e7a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="37e7a-136">NOTES</span></span>

## <span data-ttu-id="37e7a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37e7a-137">RELATED LINKS</span></span>

[<span data-ttu-id="37e7a-138">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="37e7a-138">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="37e7a-139">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="37e7a-139">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="37e7a-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="37e7a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


