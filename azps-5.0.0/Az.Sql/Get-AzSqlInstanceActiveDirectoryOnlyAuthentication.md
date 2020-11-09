---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 10788eea0c3571450a483888945ab591d7ddf13b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315617"
---
# <span data-ttu-id="3b340-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3b340-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="3b340-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b340-102">SYNOPSIS</span></span>
<span data-ttu-id="3b340-103">Получает единственную проверку подлинности в Azure AD для определенного управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="3b340-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="3b340-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b340-104">SYNTAX</span></span>

### <span data-ttu-id="3b340-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b340-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b340-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b340-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b340-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b340-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b340-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b340-108">DESCRIPTION</span></span>
<span data-ttu-id="3b340-109">Командлет **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** получает требование проверки подлинности для экземпляра Azure Active Directory (Azure AD) только для управляемых экземпляров AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="3b340-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="3b340-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b340-110">EXAMPLES</span></span>

### <span data-ttu-id="3b340-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b340-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="3b340-112">Эта команда возвращает Azure Active Directory (Azure AD) только требование проверки подлинности для управляемого экземпляра AzureSQL с именем ManagedInstance01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3b340-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3b340-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b340-113">PARAMETERS</span></span>

### <span data-ttu-id="3b340-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b340-114">-DefaultProfile</span></span>
<span data-ttu-id="3b340-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b340-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b340-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b340-116">-InputObject</span></span>
<span data-ttu-id="3b340-117">Используемый объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3b340-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="3b340-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3b340-118">-InstanceName</span></span>
<span data-ttu-id="3b340-119">Имя управляемого экземпляра Azure SQL, для которого включена проверка подлинности в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3b340-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="3b340-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b340-120">-ResourceGroupName</span></span>
<span data-ttu-id="3b340-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b340-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="3b340-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b340-122">-ResourceId</span></span>
<span data-ttu-id="3b340-123">Идентификатор ресурса используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3b340-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="3b340-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b340-124">-Confirm</span></span>
<span data-ttu-id="3b340-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b340-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b340-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b340-126">-WhatIf</span></span>
<span data-ttu-id="3b340-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b340-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b340-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b340-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b340-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b340-129">CommonParameters</span></span>
<span data-ttu-id="3b340-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b340-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b340-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b340-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b340-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b340-132">INPUTS</span></span>

### <span data-ttu-id="3b340-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3b340-133">System.String</span></span>

## <span data-ttu-id="3b340-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b340-134">OUTPUTS</span></span>

### <span data-ttu-id="3b340-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="3b340-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="3b340-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b340-136">NOTES</span></span>

## <span data-ttu-id="3b340-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b340-137">RELATED LINKS</span></span>

[<span data-ttu-id="3b340-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3b340-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3b340-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3b340-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3b340-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3b340-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="3b340-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3b340-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

