---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567684"
---
# <span data-ttu-id="dc341-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dc341-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="dc341-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc341-102">SYNOPSIS</span></span>
<span data-ttu-id="dc341-103">Удаляет экземпляр управляемой базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="dc341-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc341-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc341-104">SYNTAX</span></span>

### <span data-ttu-id="dc341-105">RemoveInstanceFromInputParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc341-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc341-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="dc341-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc341-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="dc341-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc341-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc341-108">DESCRIPTION</span></span>
<span data-ttu-id="dc341-109">Командлет **Remove-AzureRmSqlInstance** удаляет управляемый экземпляр базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dc341-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="dc341-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc341-110">EXAMPLES</span></span>

### <span data-ttu-id="dc341-111">Пример 1: удаление экземпляра</span><span class="sxs-lookup"><span data-stu-id="dc341-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dc341-112">Эта команда удаляет экземпляр с именем managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="dc341-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="dc341-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc341-113">PARAMETERS</span></span>

### <span data-ttu-id="dc341-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc341-114">-DefaultProfile</span></span>
<span data-ttu-id="dc341-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc341-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc341-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dc341-116">-Force</span></span>
<span data-ttu-id="dc341-117">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="dc341-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="dc341-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc341-118">-InputObject</span></span>
<span data-ttu-id="dc341-119">Объект AzureSqlManagedInstanceModel, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dc341-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc341-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc341-120">-Name</span></span>
<span data-ttu-id="dc341-121">Имя экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="dc341-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc341-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc341-122">-ResourceGroupName</span></span>
<span data-ttu-id="dc341-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc341-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc341-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc341-124">-ResourceId</span></span>
<span data-ttu-id="dc341-125">Идентификатор ресурса объекта экземпляра, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dc341-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc341-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc341-126">-Confirm</span></span>
<span data-ttu-id="dc341-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc341-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc341-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc341-128">-WhatIf</span></span>
<span data-ttu-id="dc341-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc341-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc341-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc341-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc341-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc341-131">CommonParameters</span></span>
<span data-ttu-id="dc341-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc341-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc341-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc341-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc341-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc341-134">INPUTS</span></span>

### <span data-ttu-id="dc341-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="dc341-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="dc341-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dc341-136">System.String</span></span>

## <span data-ttu-id="dc341-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc341-137">OUTPUTS</span></span>

### <span data-ttu-id="dc341-138">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="dc341-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="dc341-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc341-139">NOTES</span></span>

## <span data-ttu-id="dc341-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc341-140">RELATED LINKS</span></span>
