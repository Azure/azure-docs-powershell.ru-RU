---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceadvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceAdvancedDataSecurity.md
ms.openlocfilehash: 278c80206e1221550afc5c603c618c8219ea152f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905897"
---
# <span data-ttu-id="96089-101">Enable-AzSqlInstanceAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="96089-101">Enable-AzSqlInstanceAdvancedDataSecurity</span></span>

## <span data-ttu-id="96089-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96089-102">SYNOPSIS</span></span>
<span data-ttu-id="96089-103">Обеспечивает расширенную защиту данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="96089-103">Enables Advanced Data Security on a managed instance.</span></span>

## <span data-ttu-id="96089-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96089-104">SYNTAX</span></span>

```
Enable-AzSqlInstanceAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlManagedInstanceModel>] -InstanceName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96089-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96089-105">DESCRIPTION</span></span>
<span data-ttu-id="96089-106">Командлет **Enable-AzSqlInstanceAdvancedDataSecurity** обеспечивает повышенную безопасность данных на управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="96089-106">The **Enable-AzSqlInstanceAdvancedDataSecurity** cmdlet enables Advanced Data Security on a managed instance.</span></span> <span data-ttu-id="96089-107">Улучшенная безопасность данных — это единый пакет безопасности, который включает в себя классификацию данных, оценку уязвимости и улучшенную защиту угроз для управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="96089-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your managed instance.</span></span> <span data-ttu-id="96089-108">(Новая учетная запись хранилища будет создана автоматически для сохранения оценки уязвимостей.</span><span class="sxs-lookup"><span data-stu-id="96089-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="96089-109">Если ранее была создана учетная запись хранения для этой цели, она будет использоваться вместо нее.</span><span class="sxs-lookup"><span data-stu-id="96089-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="96089-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96089-110">EXAMPLES</span></span>

### <span data-ttu-id="96089-111">Пример 1: Включение расширенной защиты данных управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="96089-111">Example 1 - Enable managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlInstanceAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" 

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="96089-112">Пример 2: Включение расширенной защиты данных управляемого экземпляра с помощью ресурсов сервера</span><span class="sxs-lookup"><span data-stu-id="96089-112">Example 2 - Enable managed instance Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Enable-AzSqlInstanceAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="96089-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96089-113">PARAMETERS</span></span>

### <span data-ttu-id="96089-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96089-114">-AsJob</span></span>
<span data-ttu-id="96089-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="96089-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96089-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96089-116">-DefaultProfile</span></span>
<span data-ttu-id="96089-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96089-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96089-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="96089-118">-DeploymentName</span></span>
<span data-ttu-id="96089-119">Предоставление настраиваемого имени для развертывания расширенной безопасности данных</span><span class="sxs-lookup"><span data-stu-id="96089-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="96089-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="96089-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="96089-121">Не включать функцию автоматического устранения уязвимостей (это не приведет к созданию учетной записи хранения)</span><span class="sxs-lookup"><span data-stu-id="96089-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="96089-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96089-122">-InputObject</span></span>
<span data-ttu-id="96089-123">Объект управляемого экземпляра для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="96089-123">The managed instance object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="96089-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="96089-124">-InstanceName</span></span>
<span data-ttu-id="96089-125">Имя экземпляра управляемой базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="96089-125">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="96089-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96089-126">-ResourceGroupName</span></span>
<span data-ttu-id="96089-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96089-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="96089-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96089-128">-Confirm</span></span>
<span data-ttu-id="96089-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96089-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96089-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96089-130">-WhatIf</span></span>
<span data-ttu-id="96089-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96089-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96089-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96089-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96089-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96089-133">CommonParameters</span></span>
<span data-ttu-id="96089-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96089-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96089-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96089-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96089-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96089-136">INPUTS</span></span>

### <span data-ttu-id="96089-137">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="96089-137">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="96089-138">System. String</span><span class="sxs-lookup"><span data-stu-id="96089-138">System.String</span></span>

## <span data-ttu-id="96089-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96089-139">OUTPUTS</span></span>

### <span data-ttu-id="96089-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="96089-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="96089-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="96089-141">NOTES</span></span>

## <span data-ttu-id="96089-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96089-142">RELATED LINKS</span></span>
