---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 981baf0b0cd4d3ca70d18ab43b08bb2a16f7708f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912614"
---
# <span data-ttu-id="5344f-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="5344f-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="5344f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5344f-102">SYNOPSIS</span></span>
<span data-ttu-id="5344f-103">Обеспечивает расширенную защиту данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="5344f-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="5344f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5344f-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5344f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5344f-105">DESCRIPTION</span></span>
<span data-ttu-id="5344f-106">Командлет **Enable-AzSqlInstanceAdvancedDataSecurity** обеспечивает повышенную безопасность данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="5344f-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="5344f-107">Улучшенная безопасность данных — это единый пакет безопасности, который включает в себя классификацию данных, оценку уязвимости и улучшенную защиту угроз для управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5344f-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="5344f-108">(Новая учетная запись хранилища будет создана автоматически для сохранения оценки уязвимостей.</span><span class="sxs-lookup"><span data-stu-id="5344f-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="5344f-109">Если ранее была создана учетная запись хранения для этой цели, она будет использоваться вместо нее.</span><span class="sxs-lookup"><span data-stu-id="5344f-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="5344f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5344f-110">EXAMPLES</span></span>

### <span data-ttu-id="5344f-111">Пример 1: Включение расширенной защиты данных управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="5344f-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="5344f-112">Пример 2: Включение расширенной защиты данных управляемого экземпляра с помощью ресурсов сервера</span><span class="sxs-lookup"><span data-stu-id="5344f-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="5344f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5344f-113">PARAMETERS</span></span>

### <span data-ttu-id="5344f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5344f-114">-AsJob</span></span>
<span data-ttu-id="5344f-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5344f-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5344f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5344f-116">-DefaultProfile</span></span>
<span data-ttu-id="5344f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5344f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5344f-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="5344f-118">-DeploymentName</span></span>
<span data-ttu-id="5344f-119">Предоставление настраиваемого имени для развертывания расширенной безопасности данных</span><span class="sxs-lookup"><span data-stu-id="5344f-119">Supply a custom name for Advanced Data Security deployment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5344f-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="5344f-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="5344f-121">Не включать функцию автоматического устранения уязвимостей (это не приведет к созданию учетной записи хранения)</span><span class="sxs-lookup"><span data-stu-id="5344f-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5344f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5344f-122">-InputObject</span></span>
<span data-ttu-id="5344f-123">Объект управляемого экземпляра для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="5344f-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="5344f-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5344f-124">-InstanceName</span></span>
<span data-ttu-id="5344f-125">Имя экземпляра управляемой базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5344f-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="5344f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5344f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5344f-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5344f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="5344f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5344f-128">-Confirm</span></span>
<span data-ttu-id="5344f-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5344f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5344f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5344f-130">-WhatIf</span></span>
<span data-ttu-id="5344f-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5344f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5344f-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5344f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5344f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5344f-133">CommonParameters</span></span>
<span data-ttu-id="5344f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5344f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5344f-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5344f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5344f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5344f-136">INPUTS</span></span>

### <span data-ttu-id="5344f-137">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="5344f-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="5344f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5344f-138">System.String</span></span>

## <span data-ttu-id="5344f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5344f-139">OUTPUTS</span></span>

### <span data-ttu-id="5344f-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5344f-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="5344f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5344f-141">NOTES</span></span>

## <span data-ttu-id="5344f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5344f-142">RELATED LINKS</span></span>
