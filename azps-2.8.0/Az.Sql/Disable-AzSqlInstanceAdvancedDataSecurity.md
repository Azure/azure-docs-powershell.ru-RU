---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: a5aa9029e9d787311bb5b0c13b761c14f2b8bbca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905210"
---
# <span data-ttu-id="b529e-101">Disable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="b529e-101">Disable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="b529e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b529e-102">SYNOPSIS</span></span>
<span data-ttu-id="b529e-103">Отключение расширенной защиты данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="b529e-103">Disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="b529e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b529e-104">SYNTAX</span></span>

```
Disable-AzSqlInstanceAdvancedDataSecurity [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b529e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b529e-105">DESCRIPTION</span></span>
<span data-ttu-id="b529e-106">Командлет **Disable-AzSqlInstanceAdvancedDataSecurity** отключает расширенную защиту данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="b529e-106">The **Disable-AzSqlInstanceAdvancedDataSecurity** cmdlet disables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="b529e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b529e-107">EXAMPLES</span></span>

### <span data-ttu-id="b529e-108">Пример 1: отключение расширенной защиты данных управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="b529e-108">Example 1 - Disable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

### <span data-ttu-id="b529e-109">Пример 2: отключение расширенной защиты данных сервера от управляемого ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="b529e-109">Example 2 - Disable server Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Disable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : False
```

## <span data-ttu-id="b529e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b529e-110">PARAMETERS</span></span>

### <span data-ttu-id="b529e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b529e-111">-DefaultProfile</span></span>
<span data-ttu-id="b529e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b529e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b529e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b529e-113">-InputObject</span></span>
<span data-ttu-id="b529e-114">Объект управляемого экземпляра для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="b529e-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="b529e-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b529e-115">-InstanceName</span></span>
<span data-ttu-id="b529e-116">Имя экземпляра управляемой базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="b529e-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="b529e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b529e-117">-ResourceGroupName</span></span>
<span data-ttu-id="b529e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b529e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b529e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b529e-119">-Confirm</span></span>
<span data-ttu-id="b529e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b529e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b529e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b529e-121">-WhatIf</span></span>
<span data-ttu-id="b529e-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b529e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b529e-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b529e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b529e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b529e-124">CommonParameters</span></span>
<span data-ttu-id="b529e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b529e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b529e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b529e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b529e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b529e-127">INPUTS</span></span>

### <span data-ttu-id="b529e-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b529e-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="b529e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b529e-129">System.String</span></span>

## <span data-ttu-id="b529e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b529e-130">OUTPUTS</span></span>

### <span data-ttu-id="b529e-131">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b529e-131">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="b529e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b529e-132">NOTES</span></span>

## <span data-ttu-id="b529e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b529e-133">RELATED LINKS</span></span>
