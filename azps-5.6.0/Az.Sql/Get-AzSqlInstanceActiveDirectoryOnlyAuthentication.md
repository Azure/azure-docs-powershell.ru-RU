---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 0a06eae51b074cefb74b2ef3a175a056cc52ff84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014547"
---
# <span data-ttu-id="73af4-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="73af4-101">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="73af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73af4-102">SYNOPSIS</span></span>
<span data-ttu-id="73af4-103">Получает проверку подлинности Azure AD только для определенного SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="73af4-103">Gets Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="73af4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73af4-104">SYNTAX</span></span>

### <span data-ttu-id="73af4-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73af4-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73af4-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73af4-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73af4-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73af4-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73af4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73af4-108">DESCRIPTION</span></span>
<span data-ttu-id="73af4-109">Для управляемого экземпляра AzureSQL в текущей подписке для azure Active Directory требуется только проверка подлинности с использованием **cmdletOnlyAuthentication Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.**</span><span class="sxs-lookup"><span data-stu-id="73af4-109">The **Get-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="73af4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73af4-110">EXAMPLES</span></span>

### <span data-ttu-id="73af4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73af4-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
```

<span data-ttu-id="73af4-112">Эта команда получает только требование проверки подлинности Azure Active Directory (Azure AD) для управляемого экземпляра AzureSQL ManagedInstance01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="73af4-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="73af4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73af4-113">PARAMETERS</span></span>

### <span data-ttu-id="73af4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73af4-114">-DefaultProfile</span></span>
<span data-ttu-id="73af4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73af4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73af4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73af4-116">-InputObject</span></span>
<span data-ttu-id="73af4-117">Объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="73af4-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="73af4-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="73af4-118">-InstanceName</span></span>
<span data-ttu-id="73af4-119">Имя управляемого экземпляра Azure SQL только для проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="73af4-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="73af4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73af4-120">-ResourceGroupName</span></span>
<span data-ttu-id="73af4-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73af4-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="73af4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73af4-122">-ResourceId</span></span>
<span data-ttu-id="73af4-123">ИД используемого экземпляра ресурса</span><span class="sxs-lookup"><span data-stu-id="73af4-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="73af4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73af4-124">-Confirm</span></span>
<span data-ttu-id="73af4-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73af4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73af4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73af4-126">-WhatIf</span></span>
<span data-ttu-id="73af4-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73af4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73af4-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="73af4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73af4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73af4-129">CommonParameters</span></span>
<span data-ttu-id="73af4-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73af4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73af4-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73af4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73af4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73af4-132">INPUTS</span></span>

### <span data-ttu-id="73af4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="73af4-133">System.String</span></span>

## <span data-ttu-id="73af4-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73af4-134">OUTPUTS</span></span>

### <span data-ttu-id="73af4-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="73af4-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="73af4-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73af4-136">NOTES</span></span>

## <span data-ttu-id="73af4-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73af4-137">RELATED LINKS</span></span>

[<span data-ttu-id="73af4-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="73af4-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="73af4-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="73af4-139">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="73af4-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="73af4-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="73af4-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="73af4-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

