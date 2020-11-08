---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245656"
---
# <span data-ttu-id="d1b93-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="d1b93-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="d1b93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1b93-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b93-103">Отработка отказа управляемый экземпляр Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d1b93-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="d1b93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1b93-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1b93-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1b93-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b93-106">Командлет **Invoke-AzSqlInstanceFailover** отработка отказа управляемого экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d1b93-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="d1b93-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1b93-107">EXAMPLES</span></span>

### <span data-ttu-id="d1b93-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1b93-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="d1b93-109">Эта команда будет отработка отказа основной реплики экземпляра с именем "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="d1b93-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="d1b93-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d1b93-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="d1b93-111">Эта команда отменяет отработку отказа для считывания вторичной реплики управляемого экземпляра "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="d1b93-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="d1b93-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1b93-112">PARAMETERS</span></span>

### <span data-ttu-id="d1b93-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1b93-113">-AsJob</span></span>
<span data-ttu-id="d1b93-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d1b93-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1b93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b93-115">-DefaultProfile</span></span>
<span data-ttu-id="d1b93-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b93-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1b93-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d1b93-117">-Force</span></span>
<span data-ttu-id="d1b93-118">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="d1b93-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d1b93-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1b93-119">-Name</span></span>
<span data-ttu-id="d1b93-120">Имя удаляемого экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d1b93-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1b93-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1b93-121">-PassThru</span></span>
<span data-ttu-id="d1b93-122">При успешном выполнении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="d1b93-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="d1b93-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d1b93-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1b93-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="d1b93-124">-ReadableSecondary</span></span>
<span data-ttu-id="d1b93-125">Отработка отказа для восприятия вторичной реплики вместо основной реплики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d1b93-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="d1b93-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1b93-126">-ResourceGroupName</span></span>
<span data-ttu-id="d1b93-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1b93-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1b93-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1b93-128">-Confirm</span></span>
<span data-ttu-id="d1b93-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1b93-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1b93-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b93-130">-WhatIf</span></span>
<span data-ttu-id="d1b93-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d1b93-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1b93-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1b93-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1b93-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b93-133">CommonParameters</span></span>
<span data-ttu-id="d1b93-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1b93-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b93-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1b93-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b93-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1b93-136">INPUTS</span></span>

### <span data-ttu-id="d1b93-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d1b93-137">System.String</span></span>

## <span data-ttu-id="d1b93-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1b93-138">OUTPUTS</span></span>

## <span data-ttu-id="d1b93-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1b93-139">NOTES</span></span>

## <span data-ttu-id="d1b93-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1b93-140">RELATED LINKS</span></span>
