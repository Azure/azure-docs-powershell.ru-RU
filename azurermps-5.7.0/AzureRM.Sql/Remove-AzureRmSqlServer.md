---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 76b4e024f5a6d5979bbcd9aa860caee823ecc28e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563275"
---
# <span data-ttu-id="60add-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="60add-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="60add-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="60add-102">SYNOPSIS</span></span>
<span data-ttu-id="60add-103">Удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="60add-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60add-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="60add-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60add-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60add-105">DESCRIPTION</span></span>
<span data-ttu-id="60add-106">Командлет **Remove-AzureRmSqlServer** удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="60add-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="60add-107">Операция удаления является асинхронной и может занять некоторое время, поэтому перед выполнением каких – либо дополнительных операций, зависящих от того, что сервер удаляется, необходимо проверить, не завершилась ли операция.</span><span class="sxs-lookup"><span data-stu-id="60add-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="60add-108">Например, вам нужно создать новый сервер с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="60add-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="60add-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="60add-109">EXAMPLES</span></span>

### <span data-ttu-id="60add-110">Пример 1: Удаление сервера</span><span class="sxs-lookup"><span data-stu-id="60add-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="60add-111">Эта команда удаляет сервер базы данных SQL Azure с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="60add-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="60add-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="60add-112">PARAMETERS</span></span>

### <span data-ttu-id="60add-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60add-113">-DefaultProfile</span></span>
<span data-ttu-id="60add-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="60add-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60add-115">-Force</span><span class="sxs-lookup"><span data-stu-id="60add-115">-Force</span></span>
<span data-ttu-id="60add-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="60add-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="60add-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60add-117">-ResourceGroupName</span></span>
<span data-ttu-id="60add-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="60add-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="60add-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="60add-119">-ServerName</span></span>
<span data-ttu-id="60add-120">Указывает имя сервера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="60add-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60add-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60add-121">-Confirm</span></span>
<span data-ttu-id="60add-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="60add-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60add-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60add-123">-WhatIf</span></span>
<span data-ttu-id="60add-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="60add-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60add-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="60add-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60add-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60add-126">CommonParameters</span></span>
<span data-ttu-id="60add-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="60add-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60add-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60add-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60add-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="60add-129">INPUTS</span></span>

### <span data-ttu-id="60add-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="60add-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="60add-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="60add-131">OUTPUTS</span></span>

### <span data-ttu-id="60add-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="60add-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="60add-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="60add-133">NOTES</span></span>

## <span data-ttu-id="60add-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60add-134">RELATED LINKS</span></span>

[<span data-ttu-id="60add-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="60add-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="60add-136">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="60add-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="60add-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="60add-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="60add-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="60add-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


