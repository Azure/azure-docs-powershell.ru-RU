---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245200"
---
# <span data-ttu-id="cafc5-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="cafc5-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="cafc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cafc5-102">SYNOPSIS</span></span>
<span data-ttu-id="cafc5-103">Обеспечивается проверка подлинности в Azure AD для определенного управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="cafc5-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="cafc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cafc5-104">SYNTAX</span></span>

### <span data-ttu-id="cafc5-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cafc5-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cafc5-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cafc5-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cafc5-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cafc5-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cafc5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cafc5-108">DESCRIPTION</span></span>
<span data-ttu-id="cafc5-109">Командлет **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** включает Azure Active Directory (Azure AD) только для проверки подлинности для экземпляра, управляемого AzureSQL, в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="cafc5-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="cafc5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cafc5-110">EXAMPLES</span></span>

### <span data-ttu-id="cafc5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cafc5-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="cafc5-112">Эта команда активизирует Azure Active Directory (Azure AD) только требованием проверки подлинности для управляемого экземпляра AzureSQL с именем ManagedInstance01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="cafc5-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="cafc5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cafc5-113">PARAMETERS</span></span>

### <span data-ttu-id="cafc5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafc5-114">-DefaultProfile</span></span>
<span data-ttu-id="cafc5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cafc5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cafc5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cafc5-116">-InputObject</span></span>
<span data-ttu-id="cafc5-117">Используемый объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cafc5-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cafc5-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cafc5-118">-InstanceName</span></span>
<span data-ttu-id="cafc5-119">Имя управляемого экземпляра Azure SQL, для которого включена проверка подлинности в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cafc5-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafc5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cafc5-120">-ResourceGroupName</span></span>
<span data-ttu-id="cafc5-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cafc5-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafc5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cafc5-122">-ResourceId</span></span>
<span data-ttu-id="cafc5-123">Идентификатор ресурса используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cafc5-123">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cafc5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cafc5-124">-Confirm</span></span>
<span data-ttu-id="cafc5-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cafc5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cafc5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cafc5-126">-WhatIf</span></span>
<span data-ttu-id="cafc5-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cafc5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cafc5-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cafc5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cafc5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafc5-129">CommonParameters</span></span>
<span data-ttu-id="cafc5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cafc5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafc5-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cafc5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafc5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cafc5-132">INPUTS</span></span>

### <span data-ttu-id="cafc5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cafc5-133">System.String</span></span>

## <span data-ttu-id="cafc5-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cafc5-134">OUTPUTS</span></span>

### <span data-ttu-id="cafc5-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="cafc5-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="cafc5-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="cafc5-136">NOTES</span></span>

## <span data-ttu-id="cafc5-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cafc5-137">RELATED LINKS</span></span>

[<span data-ttu-id="cafc5-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="cafc5-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="cafc5-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="cafc5-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="cafc5-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="cafc5-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="cafc5-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="cafc5-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)