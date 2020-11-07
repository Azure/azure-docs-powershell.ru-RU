---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 6a1d69beaf6178326376278788cef612bf71c15f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906697"
---
# <span data-ttu-id="f09f4-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f09f4-101">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="f09f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f09f4-102">SYNOPSIS</span></span>
<span data-ttu-id="f09f4-103">Получение сведений об администраторе Azure AD для управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="f09f4-103">Gets information about an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="f09f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f09f4-104">SYNTAX</span></span>

### <span data-ttu-id="f09f4-105">UseResourceGroupAndInstanceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f09f4-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f09f4-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f09f4-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-InputObject <AzureSqlManagedInstanceModel>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f09f4-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f09f4-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceActiveDirectoryAdministrator [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f09f4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f09f4-108">DESCRIPTION</span></span>
<span data-ttu-id="f09f4-109">Командлет **Get-AzSqlInstanceActiveDirectoryAdministrator** получает сведения о администраторе Azure Active Directory (Azure AD) для управляемого экземпляра AzureSQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="f09f4-109">The **Get-AzSqlInstanceActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="f09f4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f09f4-110">EXAMPLES</span></span>

### <span data-ttu-id="f09f4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f09f4-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="f09f4-112">Эта команда получает сведения о администраторе Azure AD для управляемого экземпляра с именем ManagedInstance01, связанного с группой ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f09f4-112">This command gets information about an Azure AD administrator for a managed instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="f09f4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f09f4-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="f09f4-114">Эта команда получает сведения об администраторе Azure AD из объекта управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f09f4-114">This command gets information about an Azure AD administrator from a managed instance object.</span></span>

### <span data-ttu-id="f09f4-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f09f4-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Get-AzSqlInstanceActiveDirectoryAdministrator
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="f09f4-116">Эта команда получает сведения об администраторе Azure Active Directory с помощью идентификатора ресурса управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f09f4-116">This command gets information about an Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="f09f4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f09f4-117">PARAMETERS</span></span>

### <span data-ttu-id="f09f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09f4-118">-DefaultProfile</span></span>
<span data-ttu-id="f09f4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f09f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f09f4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f09f4-120">-InputObject</span></span>
<span data-ttu-id="f09f4-121">Используемый объект управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f09f4-121">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f09f4-122">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f09f4-122">-InstanceName</span></span>
<span data-ttu-id="f09f4-123">Имя экземпляра с управляемым SQL.</span><span class="sxs-lookup"><span data-stu-id="f09f4-123">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="f09f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f09f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f09f4-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f09f4-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f09f4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f09f4-126">-ResourceId</span></span>
<span data-ttu-id="f09f4-127">Идентификатор ресурса используемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f09f4-127">The resource id of instance to use</span></span>

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

### <span data-ttu-id="f09f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09f4-128">CommonParameters</span></span>
<span data-ttu-id="f09f4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f09f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09f4-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f09f4-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09f4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f09f4-131">INPUTS</span></span>

### <span data-ttu-id="f09f4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f09f4-132">System.String</span></span>

## <span data-ttu-id="f09f4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f09f4-133">OUTPUTS</span></span>

### <span data-ttu-id="f09f4-134">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="f09f4-134">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="f09f4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f09f4-135">NOTES</span></span>

## <span data-ttu-id="f09f4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f09f4-136">RELATED LINKS</span></span>

[<span data-ttu-id="f09f4-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f09f4-137">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="f09f4-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f09f4-138">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
