---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065048"
---
# <span data-ttu-id="9dd06-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="9dd06-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="9dd06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dd06-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd06-103">Получает действия для конфигурации восстановления системы сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="9dd06-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="9dd06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dd06-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dd06-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dd06-105">DESCRIPTION</span></span>
<span data-ttu-id="9dd06-106">Командлет **Get-AzSqlServerDisasterRecoveryConfigurationActivity** получает действия для конфигурации восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="9dd06-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="9dd06-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dd06-107">EXAMPLES</span></span>

## <span data-ttu-id="9dd06-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dd06-108">PARAMETERS</span></span>

### <span data-ttu-id="9dd06-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd06-109">-DefaultProfile</span></span>
<span data-ttu-id="9dd06-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9dd06-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dd06-111">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="9dd06-111">-OperationId</span></span>
<span data-ttu-id="9dd06-112">Указывает идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="9dd06-112">Specifies the operation ID.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dd06-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd06-113">-ResourceGroupName</span></span>
<span data-ttu-id="9dd06-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9dd06-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9dd06-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9dd06-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="9dd06-116">Указывает имя конфигурации восстановления системы сервера.</span><span class="sxs-lookup"><span data-stu-id="9dd06-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="9dd06-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9dd06-117">-ServerName</span></span>
<span data-ttu-id="9dd06-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9dd06-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9dd06-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dd06-119">-Confirm</span></span>
<span data-ttu-id="9dd06-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9dd06-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dd06-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dd06-121">-WhatIf</span></span>
<span data-ttu-id="9dd06-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9dd06-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dd06-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9dd06-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dd06-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd06-124">CommonParameters</span></span>
<span data-ttu-id="9dd06-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dd06-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd06-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dd06-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd06-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dd06-127">INPUTS</span></span>

### <span data-ttu-id="9dd06-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9dd06-128">System.String</span></span>

### <span data-ttu-id="9dd06-129">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9dd06-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9dd06-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dd06-130">OUTPUTS</span></span>

### <span data-ttu-id="9dd06-131">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="9dd06-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="9dd06-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dd06-132">NOTES</span></span>

## <span data-ttu-id="9dd06-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dd06-133">RELATED LINKS</span></span>

[<span data-ttu-id="9dd06-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9dd06-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
