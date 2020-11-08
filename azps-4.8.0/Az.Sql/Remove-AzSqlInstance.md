---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243909"
---
# <span data-ttu-id="5d3d0-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5d3d0-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="5d3d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d3d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5d3d0-103">Удаляет экземпляр управляемой базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="5d3d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d3d0-104">SYNTAX</span></span>

### <span data-ttu-id="5d3d0-105">RemoveInstanceFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d3d0-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3d0-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="5d3d0-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d3d0-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="5d3d0-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d3d0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d3d0-108">DESCRIPTION</span></span>
<span data-ttu-id="5d3d0-109">Командлет **Remove-AzSqlInstance** удаляет управляемый экземпляр базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="5d3d0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d3d0-110">EXAMPLES</span></span>

### <span data-ttu-id="5d3d0-111">Пример 1: удаление экземпляра</span><span class="sxs-lookup"><span data-stu-id="5d3d0-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5d3d0-112">Эта команда удаляет экземпляр с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="5d3d0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d3d0-113">PARAMETERS</span></span>

### <span data-ttu-id="5d3d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3d0-114">-DefaultProfile</span></span>
<span data-ttu-id="5d3d0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d3d0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5d3d0-116">-Force</span></span>
<span data-ttu-id="5d3d0-117">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="5d3d0-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5d3d0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d3d0-118">-InputObject</span></span>
<span data-ttu-id="5d3d0-119">Объект AzureSqlManagedInstanceModel, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d3d0-120">-Name</span></span>
<span data-ttu-id="5d3d0-121">Имя экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d3d0-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d3d0-124">-ResourceId</span></span>
<span data-ttu-id="5d3d0-125">Идентификатор ресурса объекта экземпляра, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d3d0-126">-Confirm</span></span>
<span data-ttu-id="5d3d0-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d3d0-128">-WhatIf</span></span>
<span data-ttu-id="5d3d0-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d3d0-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d3d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3d0-131">CommonParameters</span></span>
<span data-ttu-id="5d3d0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d3d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3d0-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d3d0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3d0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d3d0-134">INPUTS</span></span>

### <span data-ttu-id="5d3d0-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="5d3d0-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="5d3d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5d3d0-136">System.String</span></span>

## <span data-ttu-id="5d3d0-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d3d0-137">OUTPUTS</span></span>

### <span data-ttu-id="5d3d0-138">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="5d3d0-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="5d3d0-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d3d0-139">NOTES</span></span>

## <span data-ttu-id="5d3d0-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d3d0-140">RELATED LINKS</span></span>
