---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 0638e44f9f1c8febcbb9700fce1b9c4c9d5e410c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014563"
---
# <span data-ttu-id="a7af2-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a7af2-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="a7af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7af2-102">SYNOPSIS</span></span>
<span data-ttu-id="a7af2-103">Сведения о администраторе Azure AD для SQL управляемым экземпляром.</span><span class="sxs-lookup"><span data-stu-id="a7af2-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="a7af2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7af2-104">SYNTAX</span></span>

### <span data-ttu-id="a7af2-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7af2-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7af2-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7af2-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7af2-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7af2-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7af2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7af2-108">DESCRIPTION</span></span>
<span data-ttu-id="a7af2-109">Cmdlet **Get-AzSqlInstanceActiveDirectoryAdministrator** получает сведения о администраторе Azure Active Directory (Azure AD) для экземпляра AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a7af2-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="a7af2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7af2-110">EXAMPLES</span></span>

### <span data-ttu-id="a7af2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7af2-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a7af2-112">Эта команда получает сведения о администраторе Azure AD для управляемого экземпляра ManagedInstance01, связанного с группой ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a7af2-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="a7af2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a7af2-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a7af2-114">Эта команда получает сведения о администраторе Azure AD из объекта управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a7af2-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="a7af2-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a7af2-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="a7af2-116">Эта команда получает сведения о администраторе Azure AD с помощью идентификатора ресурса управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a7af2-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="a7af2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7af2-117">PARAMETERS</span></span>

### <span data-ttu-id="a7af2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7af2-118">-DefaultProfile</span></span>
<span data-ttu-id="a7af2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7af2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7af2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7af2-120">-InputObject</span></span>
<span data-ttu-id="a7af2-121">Объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a7af2-121">The managed instance object to use.</span></span>

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

### <span data-ttu-id="a7af2-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a7af2-122">-InstanceName</span></span>
<span data-ttu-id="a7af2-123">SQL управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="a7af2-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="a7af2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7af2-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7af2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7af2-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7af2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7af2-126">-ResourceId</span></span>
<span data-ttu-id="a7af2-127">ИД используемого экземпляра ресурса</span><span class="sxs-lookup"><span data-stu-id="a7af2-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="a7af2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7af2-128">CommonParameters</span></span>
<span data-ttu-id="a7af2-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7af2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7af2-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7af2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7af2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7af2-131">INPUTS</span></span>

### <span data-ttu-id="a7af2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a7af2-132">System.String</span></span>

## <span data-ttu-id="a7af2-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7af2-133">OUTPUTS</span></span>

### <span data-ttu-id="a7af2-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="a7af2-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="a7af2-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7af2-135">NOTES</span></span>

## <span data-ttu-id="a7af2-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7af2-136">RELATED LINKS</span></span>

[<span data-ttu-id="a7af2-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a7af2-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="a7af2-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a7af2-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
