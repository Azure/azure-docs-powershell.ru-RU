---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411172"
---
# <span data-ttu-id="a7222-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="a7222-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="a7222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7222-102">SYNOPSIS</span></span>
<span data-ttu-id="a7222-103">Отбой для управляемого экземпляра Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a7222-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="a7222-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7222-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7222-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7222-105">DESCRIPTION</span></span>
<span data-ttu-id="a7222-106">Для управляемого экземпляра Azure SQL отозвать отбой с SQL **AzSqlInstanceFailover.**</span><span class="sxs-lookup"><span data-stu-id="a7222-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="a7222-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7222-107">EXAMPLES</span></span>

### <span data-ttu-id="a7222-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7222-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="a7222-109">Эта команда отзовет основную копию экземпляра ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="a7222-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="a7222-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a7222-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="a7222-111">Эта команда отобразит учитаемую вторичную реплику управляемого экземпляра ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="a7222-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="a7222-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7222-112">PARAMETERS</span></span>

### <span data-ttu-id="a7222-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7222-113">-AsJob</span></span>
<span data-ttu-id="a7222-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a7222-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7222-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7222-115">-DefaultProfile</span></span>
<span data-ttu-id="a7222-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7222-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7222-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a7222-117">-Force</span></span>
<span data-ttu-id="a7222-118">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="a7222-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a7222-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a7222-119">-Name</span></span>
<span data-ttu-id="a7222-120">Имя экземпляра Azure SQL, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a7222-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="a7222-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7222-121">-PassThru</span></span>
<span data-ttu-id="a7222-122">При успешном выполнении возвращается истина.</span><span class="sxs-lookup"><span data-stu-id="a7222-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="a7222-123">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a7222-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7222-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="a7222-124">-ReadableSecondary</span></span>
<span data-ttu-id="a7222-125">Отбой для учитаемой вторичной реплики вместо основной реплики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a7222-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="a7222-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7222-126">-ResourceGroupName</span></span>
<span data-ttu-id="a7222-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7222-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7222-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7222-128">-Confirm</span></span>
<span data-ttu-id="a7222-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7222-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7222-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7222-130">-WhatIf</span></span>
<span data-ttu-id="a7222-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7222-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7222-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7222-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7222-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7222-133">CommonParameters</span></span>
<span data-ttu-id="a7222-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7222-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7222-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7222-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7222-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7222-136">INPUTS</span></span>

### <span data-ttu-id="a7222-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a7222-137">System.String</span></span>

## <span data-ttu-id="a7222-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7222-138">OUTPUTS</span></span>

## <span data-ttu-id="a7222-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7222-139">NOTES</span></span>

## <span data-ttu-id="a7222-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7222-140">RELATED LINKS</span></span>
