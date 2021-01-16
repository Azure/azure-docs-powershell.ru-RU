---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419535"
---
# <span data-ttu-id="86435-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="86435-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="86435-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86435-102">SYNOPSIS</span></span>
<span data-ttu-id="86435-103">Отключает advanced Data Security для управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="86435-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="86435-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86435-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86435-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86435-105">DESCRIPTION</span></span>
<span data-ttu-id="86435-106">Для управляемого экземпляра cmdlet **Disable-AzSqlInstanceAdvancedDataSecurity** отключает advanced Data Security.</span><span class="sxs-lookup"><span data-stu-id="86435-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="86435-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86435-107">EXAMPLES</span></span>

### <span data-ttu-id="86435-108">Пример 1. Отключение управляемого экземпляра Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="86435-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="86435-109">Пример 2. Отключение advanced Data Security сервера от ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="86435-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="86435-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86435-110">PARAMETERS</span></span>

### <span data-ttu-id="86435-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86435-111">-DefaultProfile</span></span>
<span data-ttu-id="86435-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86435-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86435-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86435-113">-InputObject</span></span>
<span data-ttu-id="86435-114">Объект управляемого экземпляра, который используется с операцией advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="86435-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86435-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="86435-115">-InstanceName</span></span>
<span data-ttu-id="86435-116">SQL имени экземпляра, управляемого базой данных.</span><span class="sxs-lookup"><span data-stu-id="86435-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="86435-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86435-117">-ResourceGroupName</span></span>
<span data-ttu-id="86435-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86435-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="86435-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86435-119">-Confirm</span></span>
<span data-ttu-id="86435-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="86435-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86435-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86435-121">-WhatIf</span></span>
<span data-ttu-id="86435-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86435-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86435-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="86435-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86435-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86435-124">CommonParameters</span></span>
<span data-ttu-id="86435-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86435-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86435-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86435-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86435-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86435-127">INPUTS</span></span>

### <span data-ttu-id="86435-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="86435-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="86435-129">System.String</span><span class="sxs-lookup"><span data-stu-id="86435-129">System.String</span></span>

## <span data-ttu-id="86435-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86435-130">OUTPUTS</span></span>

### <span data-ttu-id="86435-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="86435-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="86435-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86435-132">NOTES</span></span>

## <span data-ttu-id="86435-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86435-133">RELATED LINKS</span></span>
