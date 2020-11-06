---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d2a92e7209745873364b5de114916bc48b0a3b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559480"
---
# <span data-ttu-id="f0998-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="f0998-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="f0998-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0998-102">SYNOPSIS</span></span>
<span data-ttu-id="f0998-103">Получает состояние обновления сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f0998-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0998-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0998-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0998-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0998-105">DESCRIPTION</span></span>
<span data-ttu-id="f0998-106">Командлет **Get-AzureRmSqlServerUpgrade** получает состояние обновления сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f0998-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="f0998-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0998-107">EXAMPLES</span></span>

### <span data-ttu-id="f0998-108">Пример 1: получение состояния обновления</span><span class="sxs-lookup"><span data-stu-id="f0998-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="f0998-109">Эта команда получает состояние обновления с сервера с именем Server01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f0998-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f0998-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0998-110">PARAMETERS</span></span>

### <span data-ttu-id="f0998-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0998-111">-ResourceGroupName</span></span>
<span data-ttu-id="f0998-112">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="f0998-112">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f0998-113">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f0998-113">-ServerName</span></span>
<span data-ttu-id="f0998-114">Указывает имя сервера, для которого этот командлет получает состояние обновления.</span><span class="sxs-lookup"><span data-stu-id="f0998-114">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0998-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0998-115">-Confirm</span></span>
<span data-ttu-id="f0998-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0998-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0998-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0998-117">-WhatIf</span></span>
<span data-ttu-id="f0998-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0998-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0998-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0998-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0998-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0998-120">-DefaultProfile</span></span>
<span data-ttu-id="f0998-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0998-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0998-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0998-122">CommonParameters</span></span>
<span data-ttu-id="f0998-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0998-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0998-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0998-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0998-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0998-125">INPUTS</span></span>

## <span data-ttu-id="f0998-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0998-126">OUTPUTS</span></span>

### <span data-ttu-id="f0998-127">Microsoft. Azure. Commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="f0998-127">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="f0998-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0998-128">NOTES</span></span>

## <span data-ttu-id="f0998-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0998-129">RELATED LINKS</span></span>

[<span data-ttu-id="f0998-130">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="f0998-130">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="f0998-131">Остановить-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="f0998-131">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="f0998-132">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f0998-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


