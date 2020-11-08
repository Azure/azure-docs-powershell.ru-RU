---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 5f4ee759fcfddf8e68bc41b68706ccaf2d582e96
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235313"
---
# <span data-ttu-id="de610-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="de610-101">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="de610-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de610-102">SYNOPSIS</span></span>
<span data-ttu-id="de610-103">Отключение проверки подлинности Azure AD для определенного экземпляра, управляемого SQL.</span><span class="sxs-lookup"><span data-stu-id="de610-103">Disables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="de610-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de610-104">SYNTAX</span></span>

### <span data-ttu-id="de610-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de610-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de610-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de610-106">UseInputObjectParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de610-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de610-107">UserResourceIdParameterSet</span></span>
```
Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de610-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de610-108">DESCRIPTION</span></span>
<span data-ttu-id="de610-109">Командлет **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** отключает Azure Active Directory (Azure AD) только требованием проверки подлинности для экземпляра, управляемого AzureSQL, в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="de610-109">The **Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="de610-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de610-110">EXAMPLES</span></span>

### <span data-ttu-id="de610-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de610-111">Example 1</span></span>
```powershell
PS C:\>Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="de610-112">Эта команда отключает Azure Active Directory (Azure AD) только требованием проверки подлинности для управляемого экземпляра AzureSQL с именем ManagedInstance01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="de610-112">This command disables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="de610-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de610-113">PARAMETERS</span></span>

### <span data-ttu-id="de610-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de610-114">-DefaultProfile</span></span>
<span data-ttu-id="de610-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de610-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de610-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de610-116">-InputObject</span></span>
<span data-ttu-id="de610-117">Используемый объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="de610-117">The managed instance object to use.</span></span>

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

### <span data-ttu-id="de610-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="de610-118">-InstanceName</span></span>
<span data-ttu-id="de610-119">Имя управляемого экземпляра Azure SQL, для которого включена проверка подлинности в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de610-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

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

### <span data-ttu-id="de610-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de610-120">-ResourceGroupName</span></span>
<span data-ttu-id="de610-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de610-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="de610-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de610-122">-ResourceId</span></span>
<span data-ttu-id="de610-123">Идентификатор ресурса используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="de610-123">The resource id of instance to use</span></span>

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

### <span data-ttu-id="de610-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de610-124">-Confirm</span></span>
<span data-ttu-id="de610-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de610-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de610-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de610-126">-WhatIf</span></span>
<span data-ttu-id="de610-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de610-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de610-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de610-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de610-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de610-129">CommonParameters</span></span>
<span data-ttu-id="de610-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de610-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de610-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de610-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de610-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de610-132">INPUTS</span></span>

### <span data-ttu-id="de610-133">System. String</span><span class="sxs-lookup"><span data-stu-id="de610-133">System.String</span></span>

## <span data-ttu-id="de610-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de610-134">OUTPUTS</span></span>

### <span data-ttu-id="de610-135">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="de610-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="de610-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="de610-136">NOTES</span></span>

## <span data-ttu-id="de610-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de610-137">RELATED LINKS</span></span>

[<span data-ttu-id="de610-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="de610-138">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="de610-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="de610-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="de610-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="de610-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="de610-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="de610-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)