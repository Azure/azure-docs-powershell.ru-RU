---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: faf93387f068c6ee8e83653d31b96a1f3ecdef70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729058"
---
# <span data-ttu-id="2f5ac-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="2f5ac-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="2f5ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5ac-103">Обеспечивает расширенную защиту данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="2f5ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f5ac-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f5ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f5ac-105">DESCRIPTION</span></span>
<span data-ttu-id="2f5ac-106">Командлет **Enable-AzSqlInstanceAdvancedDataSecurity** обеспечивает повышенную безопасность данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="2f5ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f5ac-107">EXAMPLES</span></span>

### <span data-ttu-id="2f5ac-108">Пример 1: Включение расширенной защиты данных управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="2f5ac-108">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="2f5ac-109">Пример 2: Включение расширенной защиты данных управляемого экземпляра с помощью ресурсов сервера</span><span class="sxs-lookup"><span data-stu-id="2f5ac-109">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="2f5ac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f5ac-110">PARAMETERS</span></span>

### <span data-ttu-id="2f5ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5ac-111">-DefaultProfile</span></span>
<span data-ttu-id="2f5ac-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f5ac-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f5ac-113">-InputObject</span></span>
<span data-ttu-id="2f5ac-114">Объект управляемого экземпляра для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="2f5ac-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="2f5ac-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="2f5ac-115">-InstanceName</span></span>
<span data-ttu-id="2f5ac-116">Имя экземпляра управляемой базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="2f5ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f5ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f5ac-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f5ac-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f5ac-119">-Confirm</span></span>
<span data-ttu-id="2f5ac-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f5ac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f5ac-121">-WhatIf</span></span>
<span data-ttu-id="2f5ac-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f5ac-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f5ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5ac-124">CommonParameters</span></span>
<span data-ttu-id="2f5ac-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f5ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5ac-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f5ac-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5ac-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f5ac-127">INPUTS</span></span>

### <span data-ttu-id="2f5ac-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="2f5ac-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="2f5ac-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2f5ac-129">System.String</span></span>

## <span data-ttu-id="2f5ac-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f5ac-130">OUTPUTS</span></span>

### <span data-ttu-id="2f5ac-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2f5ac-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="2f5ac-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f5ac-132">NOTES</span></span>

## <span data-ttu-id="2f5ac-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f5ac-133">RELATED LINKS</span></span>
