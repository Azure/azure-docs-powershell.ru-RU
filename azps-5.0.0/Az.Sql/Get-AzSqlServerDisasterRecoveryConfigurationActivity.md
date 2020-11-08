---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247514"
---
# <span data-ttu-id="fc0e1-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="fc0e1-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="fc0e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0e1-103">Получает действия для конфигурации восстановления системы сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="fc0e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc0e1-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc0e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc0e1-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0e1-106">Командлет **Get-AzSqlServerDisasterRecoveryConfigurationActivity** получает действия для конфигурации восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="fc0e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc0e1-107">EXAMPLES</span></span>

## <span data-ttu-id="fc0e1-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc0e1-108">PARAMETERS</span></span>

### <span data-ttu-id="fc0e1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0e1-109">-DefaultProfile</span></span>
<span data-ttu-id="fc0e1-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fc0e1-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc0e1-111">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="fc0e1-111">-OperationId</span></span>
<span data-ttu-id="fc0e1-112">Указывает идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="fc0e1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc0e1-113">-ResourceGroupName</span></span>
<span data-ttu-id="fc0e1-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fc0e1-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="fc0e1-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="fc0e1-116">Указывает имя конфигурации восстановления системы сервера.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="fc0e1-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fc0e1-117">-ServerName</span></span>
<span data-ttu-id="fc0e1-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="fc0e1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc0e1-119">-Confirm</span></span>
<span data-ttu-id="fc0e1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc0e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc0e1-121">-WhatIf</span></span>
<span data-ttu-id="fc0e1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc0e1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc0e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0e1-124">CommonParameters</span></span>
<span data-ttu-id="fc0e1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc0e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0e1-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc0e1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0e1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc0e1-127">INPUTS</span></span>

### <span data-ttu-id="fc0e1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fc0e1-128">System.String</span></span>

### <span data-ttu-id="fc0e1-129">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fc0e1-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fc0e1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc0e1-130">OUTPUTS</span></span>

### <span data-ttu-id="fc0e1-131">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="fc0e1-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="fc0e1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc0e1-132">NOTES</span></span>

## <span data-ttu-id="fc0e1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc0e1-133">RELATED LINKS</span></span>

[<span data-ttu-id="fc0e1-134">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="fc0e1-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
