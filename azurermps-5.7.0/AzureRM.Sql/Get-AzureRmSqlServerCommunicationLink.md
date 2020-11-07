---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 8240712b4ec6ef17dfff597bed4dc62d60be42b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732350"
---
# <span data-ttu-id="3df39-101">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="3df39-101">Get-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="3df39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3df39-102">SYNOPSIS</span></span>
<span data-ttu-id="3df39-103">Получает коммуникационные ссылки на транзакции эластичных баз данных между серверами баз данных.</span><span class="sxs-lookup"><span data-stu-id="3df39-103">Gets communication links for elastic database transactions between database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3df39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3df39-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3df39-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3df39-105">DESCRIPTION</span></span>
<span data-ttu-id="3df39-106">Командлет **Get-AzureRmSqlServerCommunicationLink** получает коммуникационные ссылки "сервер-сервер" для транзакций эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3df39-106">The **Get-AzureRmSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="3df39-107">Укажите имя коммуникационной ссылки на сервер, чтобы просмотреть свойства этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="3df39-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="3df39-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3df39-108">EXAMPLES</span></span>

### <span data-ttu-id="3df39-109">Пример 1: получение всех коммуникационных ссылок на сервер</span><span class="sxs-lookup"><span data-stu-id="3df39-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="3df39-110">Эта команда получает все ссылки на связь между сервером для транзакций эластичных баз данных для сервера с именем ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="3df39-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="3df39-111">Пример 2: получение специальной коммуникационной ссылки для сервера</span><span class="sxs-lookup"><span data-stu-id="3df39-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="3df39-112">Эта команда получает связь между сервером и сервером с именем Link01.</span><span class="sxs-lookup"><span data-stu-id="3df39-112">This command gets the server-to-server communication link named Link01.</span></span>

## <span data-ttu-id="3df39-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3df39-113">PARAMETERS</span></span>

### <span data-ttu-id="3df39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df39-114">-DefaultProfile</span></span>
<span data-ttu-id="3df39-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3df39-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3df39-116">-LinkName</span><span class="sxs-lookup"><span data-stu-id="3df39-116">-LinkName</span></span>
<span data-ttu-id="3df39-117">Указывает имя серверной ссылки, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3df39-117">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3df39-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df39-118">-ResourceGroupName</span></span>
<span data-ttu-id="3df39-119">Указывает имя группы ресурсов, к которой принадлежит сервер, указанный в параметре *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="3df39-119">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="3df39-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3df39-120">-ServerName</span></span>
<span data-ttu-id="3df39-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3df39-121">Specifies the name of a server.</span></span>
<span data-ttu-id="3df39-122">Этот сервер включает ссылку для связи, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3df39-122">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3df39-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3df39-123">-Confirm</span></span>
<span data-ttu-id="3df39-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3df39-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df39-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df39-125">-WhatIf</span></span>
<span data-ttu-id="3df39-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3df39-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df39-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3df39-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df39-128">CommonParameters</span></span>
<span data-ttu-id="3df39-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3df39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df39-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3df39-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df39-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3df39-131">INPUTS</span></span>

### <span data-ttu-id="3df39-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="3df39-132">None</span></span>
<span data-ttu-id="3df39-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3df39-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3df39-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3df39-134">OUTPUTS</span></span>

### <span data-ttu-id="3df39-135">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="3df39-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="3df39-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3df39-136">NOTES</span></span>
* <span data-ttu-id="3df39-137">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="3df39-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="3df39-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3df39-138">RELATED LINKS</span></span>

[<span data-ttu-id="3df39-139">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="3df39-139">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="3df39-140">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="3df39-140">Remove-AzureRmSqlServerCommunicationLink</span></span>](./Remove-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="3df39-141">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3df39-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
