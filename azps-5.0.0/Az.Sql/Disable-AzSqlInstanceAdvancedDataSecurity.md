---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 39b23c1b39121f143791667ade542080ba70ec95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246995"
---
# <span data-ttu-id="61289-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="61289-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="61289-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61289-102">SYNOPSIS</span></span>
<span data-ttu-id="61289-103">Отключение расширенной защиты данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="61289-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="61289-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61289-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61289-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61289-105">DESCRIPTION</span></span>
<span data-ttu-id="61289-106">Командлет **Disable-AzSqlInstanceAdvancedDataSecurity** отключает расширенную защиту данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="61289-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="61289-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61289-107">EXAMPLES</span></span>

### <span data-ttu-id="61289-108">Пример 1: отключение расширенной защиты данных управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="61289-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="61289-109">Пример 2: отключение расширенной защиты данных сервера от управляемого ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="61289-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="61289-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61289-110">PARAMETERS</span></span>

### <span data-ttu-id="61289-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61289-111">-DefaultProfile</span></span>
<span data-ttu-id="61289-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61289-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61289-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61289-113">-InputObject</span></span>
<span data-ttu-id="61289-114">Объект управляемого экземпляра для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="61289-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="61289-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="61289-115">-InstanceName</span></span>
<span data-ttu-id="61289-116">Имя экземпляра управляемой базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="61289-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="61289-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61289-117">-ResourceGroupName</span></span>
<span data-ttu-id="61289-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61289-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="61289-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61289-119">-Confirm</span></span>
<span data-ttu-id="61289-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61289-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61289-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61289-121">-WhatIf</span></span>
<span data-ttu-id="61289-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61289-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61289-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61289-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61289-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61289-124">CommonParameters</span></span>
<span data-ttu-id="61289-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61289-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61289-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61289-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61289-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61289-127">INPUTS</span></span>

### <span data-ttu-id="61289-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="61289-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="61289-129">System. String</span><span class="sxs-lookup"><span data-stu-id="61289-129">System.String</span></span>

## <span data-ttu-id="61289-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61289-130">OUTPUTS</span></span>

### <span data-ttu-id="61289-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="61289-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="61289-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="61289-132">NOTES</span></span>

## <span data-ttu-id="61289-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61289-133">RELATED LINKS</span></span>
