---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416284"
---
# <span data-ttu-id="470cc-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="470cc-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="470cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="470cc-102">SYNOPSIS</span></span>
<span data-ttu-id="470cc-103">Удаляет экземпляр управляемой SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="470cc-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="470cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="470cc-104">SYNTAX</span></span>

### <span data-ttu-id="470cc-105">RemoveInstanceFromInputParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="470cc-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="470cc-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="470cc-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="470cc-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="470cc-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="470cc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="470cc-108">DESCRIPTION</span></span>
<span data-ttu-id="470cc-109">Для удаления экземпляра базы данных Azure SQL удаляется SQL **AzSqlInstance.**</span><span class="sxs-lookup"><span data-stu-id="470cc-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="470cc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="470cc-110">EXAMPLES</span></span>

### <span data-ttu-id="470cc-111">Пример 1. Удаление экземпляра</span><span class="sxs-lookup"><span data-stu-id="470cc-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="470cc-112">Эта команда удаляет экземпляр ManagedInstance1.</span><span class="sxs-lookup"><span data-stu-id="470cc-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="470cc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="470cc-113">PARAMETERS</span></span>

### <span data-ttu-id="470cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470cc-114">-DefaultProfile</span></span>
<span data-ttu-id="470cc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="470cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="470cc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="470cc-116">-Force</span></span>
<span data-ttu-id="470cc-117">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="470cc-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="470cc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="470cc-118">-InputObject</span></span>
<span data-ttu-id="470cc-119">Объект AzureSqlManagedInstanceModel, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="470cc-119">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="470cc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="470cc-120">-Name</span></span>
<span data-ttu-id="470cc-121">SQL имени экземпляра.</span><span class="sxs-lookup"><span data-stu-id="470cc-121">SQL instance name.</span></span>

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

### <span data-ttu-id="470cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="470cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="470cc-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="470cc-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="470cc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="470cc-124">-ResourceId</span></span>
<span data-ttu-id="470cc-125">ИД ресурса объекта экземпляра, который требуется удалить</span><span class="sxs-lookup"><span data-stu-id="470cc-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="470cc-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="470cc-126">-Confirm</span></span>
<span data-ttu-id="470cc-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="470cc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="470cc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="470cc-128">-WhatIf</span></span>
<span data-ttu-id="470cc-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="470cc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="470cc-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="470cc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="470cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470cc-131">CommonParameters</span></span>
<span data-ttu-id="470cc-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470cc-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="470cc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470cc-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="470cc-134">INPUTS</span></span>

### <span data-ttu-id="470cc-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="470cc-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="470cc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="470cc-136">System.String</span></span>

## <span data-ttu-id="470cc-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="470cc-137">OUTPUTS</span></span>

### <span data-ttu-id="470cc-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="470cc-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="470cc-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="470cc-139">NOTES</span></span>

## <span data-ttu-id="470cc-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="470cc-140">RELATED LINKS</span></span>
