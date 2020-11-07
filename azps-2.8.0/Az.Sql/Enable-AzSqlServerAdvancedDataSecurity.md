---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: c2c3b634eb5a9e031c375a6cc696298becd58e8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905894"
---
# <span data-ttu-id="d280c-101">Enable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="d280c-101">Enable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="d280c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d280c-102">SYNOPSIS</span></span>
<span data-ttu-id="d280c-103">Обеспечивает повышенную безопасность данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="d280c-103">Enables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="d280c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d280c-104">SYNTAX</span></span>

```
Enable-AzSqlServerAdvancedDataSecurity [-DoNotConfigureVulnerabilityAssessment] [-AsJob]
 [-DeploymentName <String>] [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d280c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d280c-105">DESCRIPTION</span></span>
<span data-ttu-id="d280c-106">Командлет **Enable-AzSqlServerAdvancedDataSecurity** обеспечивает повышенную безопасность данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="d280c-106">The **Enable-AzSqlServerAdvancedDataSecurity** cmdlet enables Advanced Data Security on a server.</span></span> <span data-ttu-id="d280c-107">Улучшенная безопасность данных — это единый пакет безопасности, который включает в себя классификацию данных, оценку уязвимости и улучшенную защиту угроз для вашего сервера.</span><span class="sxs-lookup"><span data-stu-id="d280c-107">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your server.</span></span> <span data-ttu-id="d280c-108">(Новая учетная запись хранилища будет создана автоматически для сохранения оценки уязвимостей.</span><span class="sxs-lookup"><span data-stu-id="d280c-108">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="d280c-109">Если ранее была создана учетная запись хранения для этой цели, она будет использоваться вместо нее.</span><span class="sxs-lookup"><span data-stu-id="d280c-109">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="d280c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d280c-110">EXAMPLES</span></span>

### <span data-ttu-id="d280c-111">Пример 1: Включение расширенной защиты данных сервера</span><span class="sxs-lookup"><span data-stu-id="d280c-111">Example 1 - Enable server Advanced Data Security</span></span>
```powershell
PS C:\>  Enable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="d280c-112">Пример 2: Включение расширенной защиты данных сервера на серверный ресурс</span><span class="sxs-lookup"><span data-stu-id="d280c-112">Example 2 - Enable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Enable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="d280c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d280c-113">PARAMETERS</span></span>

### <span data-ttu-id="d280c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d280c-114">-AsJob</span></span>
<span data-ttu-id="d280c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d280c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d280c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d280c-116">-DefaultProfile</span></span>
<span data-ttu-id="d280c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d280c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d280c-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d280c-118">-DeploymentName</span></span>
<span data-ttu-id="d280c-119">Предоставление настраиваемого имени для развертывания расширенной безопасности данных</span><span class="sxs-lookup"><span data-stu-id="d280c-119">Supply a custom name for Advanced Data Security deployment</span></span>

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

### <span data-ttu-id="d280c-120">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="d280c-120">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="d280c-121">Не включать функцию автоматического устранения уязвимостей (это не приведет к созданию учетной записи хранения)</span><span class="sxs-lookup"><span data-stu-id="d280c-121">Do not auto enable Vulnerability Assessment (This will not create a storage account)</span></span>

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

### <span data-ttu-id="d280c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d280c-122">-InputObject</span></span>
<span data-ttu-id="d280c-123">Объект сервера для использования с расширенной операцией политики безопасности данных</span><span class="sxs-lookup"><span data-stu-id="d280c-123">The server object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d280c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d280c-124">-ResourceGroupName</span></span>
<span data-ttu-id="d280c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d280c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d280c-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d280c-126">-ServerName</span></span>
<span data-ttu-id="d280c-127">Имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d280c-127">SQL Database server name.</span></span>

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

### <span data-ttu-id="d280c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d280c-128">-Confirm</span></span>
<span data-ttu-id="d280c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d280c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d280c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d280c-130">-WhatIf</span></span>
<span data-ttu-id="d280c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d280c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d280c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d280c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d280c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d280c-133">CommonParameters</span></span>
<span data-ttu-id="d280c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d280c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d280c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d280c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d280c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d280c-136">INPUTS</span></span>

### <span data-ttu-id="d280c-137">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="d280c-137">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="d280c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d280c-138">System.String</span></span>

## <span data-ttu-id="d280c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d280c-139">OUTPUTS</span></span>

### <span data-ttu-id="d280c-140">Microsoft. Azure. Commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d280c-140">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="d280c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d280c-141">NOTES</span></span>

## <span data-ttu-id="d280c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d280c-142">RELATED LINKS</span></span>
