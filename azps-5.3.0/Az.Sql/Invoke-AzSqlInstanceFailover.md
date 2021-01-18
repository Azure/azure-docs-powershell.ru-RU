---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517122"
---
# <span data-ttu-id="0d82d-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="0d82d-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="0d82d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d82d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d82d-103">Отбой для управляемого экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0d82d-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="0d82d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0d82d-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d82d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d82d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d82d-106">Для управляемого экземпляра Azure SQL отозвать отбой с SQL **AzSqlInstanceFailover.**</span><span class="sxs-lookup"><span data-stu-id="0d82d-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="0d82d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0d82d-107">EXAMPLES</span></span>

### <span data-ttu-id="0d82d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d82d-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="0d82d-109">Эта команда отзовет основную копию экземпляра ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="0d82d-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="0d82d-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0d82d-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="0d82d-111">Эта команда отобразит учитаемую вторичную копию управляемого экземпляра ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="0d82d-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="0d82d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d82d-112">PARAMETERS</span></span>

### <span data-ttu-id="0d82d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d82d-113">-AsJob</span></span>
<span data-ttu-id="0d82d-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0d82d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d82d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d82d-115">-DefaultProfile</span></span>
<span data-ttu-id="0d82d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d82d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d82d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0d82d-117">-Force</span></span>
<span data-ttu-id="0d82d-118">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="0d82d-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0d82d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0d82d-119">-Name</span></span>
<span data-ttu-id="0d82d-120">Имя экземпляра Azure SQL, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0d82d-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="0d82d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d82d-121">-PassThru</span></span>
<span data-ttu-id="0d82d-122">При успешном выполнении возвращается истина.</span><span class="sxs-lookup"><span data-stu-id="0d82d-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="0d82d-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0d82d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d82d-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="0d82d-124">-ReadableSecondary</span></span>
<span data-ttu-id="0d82d-125">Отбой для учитаемой вторичной реплики вместо основной реплики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0d82d-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="0d82d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d82d-126">-ResourceGroupName</span></span>
<span data-ttu-id="0d82d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d82d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="0d82d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d82d-128">-Confirm</span></span>
<span data-ttu-id="0d82d-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d82d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d82d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d82d-130">-WhatIf</span></span>
<span data-ttu-id="0d82d-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d82d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d82d-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0d82d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d82d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d82d-133">CommonParameters</span></span>
<span data-ttu-id="0d82d-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d82d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d82d-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d82d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d82d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d82d-136">INPUTS</span></span>

### <span data-ttu-id="0d82d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0d82d-137">System.String</span></span>

## <span data-ttu-id="0d82d-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d82d-138">OUTPUTS</span></span>

## <span data-ttu-id="0d82d-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0d82d-139">NOTES</span></span>

## <span data-ttu-id="0d82d-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d82d-140">RELATED LINKS</span></span>
