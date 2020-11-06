---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 48b1ee50f1ebd0003097500849a6d03dac64c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570047"
---
# <span data-ttu-id="2991a-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2991a-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="2991a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2991a-102">SYNOPSIS</span></span>
<span data-ttu-id="2991a-103">Удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2991a-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2991a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2991a-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2991a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2991a-105">DESCRIPTION</span></span>
<span data-ttu-id="2991a-106">Командлет **Remove-AzureRmSqlServer** удаляет сервер базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2991a-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="2991a-107">Операция удаления является асинхронной и может занять некоторое время, поэтому перед выполнением каких – либо дополнительных операций, зависящих от того, что сервер удаляется, необходимо проверить, не завершилась ли операция.</span><span class="sxs-lookup"><span data-stu-id="2991a-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="2991a-108">Например, вам нужно создать новый сервер с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="2991a-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="2991a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2991a-109">EXAMPLES</span></span>

### <span data-ttu-id="2991a-110">Пример 1: Удаление сервера</span><span class="sxs-lookup"><span data-stu-id="2991a-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="2991a-111">Эта команда удаляет сервер базы данных SQL Azure с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="2991a-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="2991a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2991a-112">PARAMETERS</span></span>

### <span data-ttu-id="2991a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2991a-113">-Force</span></span>
<span data-ttu-id="2991a-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2991a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2991a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2991a-115">-ResourceGroupName</span></span>
<span data-ttu-id="2991a-116">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="2991a-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2991a-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2991a-117">-ServerName</span></span>
<span data-ttu-id="2991a-118">Указывает имя сервера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2991a-118">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2991a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2991a-119">-Confirm</span></span>
<span data-ttu-id="2991a-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2991a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2991a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2991a-121">-WhatIf</span></span>
<span data-ttu-id="2991a-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2991a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2991a-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2991a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2991a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2991a-124">-DefaultProfile</span></span>
<span data-ttu-id="2991a-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2991a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2991a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2991a-126">CommonParameters</span></span>
<span data-ttu-id="2991a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2991a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2991a-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2991a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2991a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2991a-129">INPUTS</span></span>

### <span data-ttu-id="2991a-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="2991a-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="2991a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2991a-131">OUTPUTS</span></span>

### <span data-ttu-id="2991a-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="2991a-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="2991a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2991a-133">NOTES</span></span>

## <span data-ttu-id="2991a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2991a-134">RELATED LINKS</span></span>

[<span data-ttu-id="2991a-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2991a-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="2991a-136">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2991a-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="2991a-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="2991a-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="2991a-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2991a-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


