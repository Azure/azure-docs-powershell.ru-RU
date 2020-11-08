---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235820"
---
# <span data-ttu-id="0d243-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="0d243-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="0d243-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d243-102">SYNOPSIS</span></span>
<span data-ttu-id="0d243-103">Отработка отказа управляемый экземпляр Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0d243-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="0d243-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d243-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d243-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d243-105">DESCRIPTION</span></span>
<span data-ttu-id="0d243-106">Командлет **Invoke-AzSqlInstanceFailover** отработка отказа управляемого экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0d243-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="0d243-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d243-107">EXAMPLES</span></span>

### <span data-ttu-id="0d243-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d243-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="0d243-109">Эта команда будет отработка отказа основной реплики экземпляра с именем "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="0d243-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="0d243-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0d243-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="0d243-111">Эта команда отменяет отработку отказа для считывания вторичной реплики управляемого экземпляра "ManagedInstance01".</span><span class="sxs-lookup"><span data-stu-id="0d243-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="0d243-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d243-112">PARAMETERS</span></span>

### <span data-ttu-id="0d243-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d243-113">-AsJob</span></span>
<span data-ttu-id="0d243-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0d243-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d243-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d243-115">-DefaultProfile</span></span>
<span data-ttu-id="0d243-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d243-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d243-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0d243-117">-Force</span></span>
<span data-ttu-id="0d243-118">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="0d243-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0d243-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d243-119">-Name</span></span>
<span data-ttu-id="0d243-120">Имя удаляемого экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0d243-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="0d243-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d243-121">-PassThru</span></span>
<span data-ttu-id="0d243-122">При успешном выполнении возвращает значение истина.</span><span class="sxs-lookup"><span data-stu-id="0d243-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="0d243-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0d243-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d243-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="0d243-124">-ReadableSecondary</span></span>
<span data-ttu-id="0d243-125">Отработка отказа для восприятия вторичной реплики вместо основной реплики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0d243-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="0d243-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d243-126">-ResourceGroupName</span></span>
<span data-ttu-id="0d243-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d243-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="0d243-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d243-128">-Confirm</span></span>
<span data-ttu-id="0d243-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d243-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d243-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d243-130">-WhatIf</span></span>
<span data-ttu-id="0d243-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d243-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d243-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d243-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d243-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d243-133">CommonParameters</span></span>
<span data-ttu-id="0d243-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d243-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d243-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d243-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d243-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d243-136">INPUTS</span></span>

### <span data-ttu-id="0d243-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0d243-137">System.String</span></span>

## <span data-ttu-id="0d243-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d243-138">OUTPUTS</span></span>

## <span data-ttu-id="0d243-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d243-139">NOTES</span></span>

## <span data-ttu-id="0d243-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d243-140">RELATED LINKS</span></span>
