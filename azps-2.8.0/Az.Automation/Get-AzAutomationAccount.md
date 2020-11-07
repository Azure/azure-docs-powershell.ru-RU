---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 6c5e0a376b8170c73abc394f275995b178e90917
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727876"
---
# <span data-ttu-id="cde62-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cde62-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="cde62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cde62-102">SYNOPSIS</span></span>
<span data-ttu-id="cde62-103">Возвращает учетные записи автоматизации в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cde62-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="cde62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cde62-104">SYNTAX</span></span>

### <span data-ttu-id="cde62-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cde62-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cde62-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cde62-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde62-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cde62-107">DESCRIPTION</span></span>
<span data-ttu-id="cde62-108">Командлет **Get-AzAutomationAccount** получает учетные записи службы автоматизации Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cde62-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="cde62-109">Дополнительные сведения об учетных записях автоматизации можно найти в командлете New-AzAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="cde62-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="cde62-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cde62-110">EXAMPLES</span></span>

### <span data-ttu-id="cde62-111">Пример 1: получение всех учетных записей</span><span class="sxs-lookup"><span data-stu-id="cde62-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="cde62-112">Эта команда получает все учетные записи автоматизации в группе ресурсов с именем ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="cde62-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="cde62-113">Пример 2: получение учетной записи</span><span class="sxs-lookup"><span data-stu-id="cde62-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="cde62-114">Эта команда получает учетную запись автоматизации с именем ContosoAutomationAccount в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cde62-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="cde62-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cde62-115">PARAMETERS</span></span>

### <span data-ttu-id="cde62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde62-116">-DefaultProfile</span></span>
<span data-ttu-id="cde62-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cde62-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cde62-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cde62-118">-Name</span></span>
<span data-ttu-id="cde62-119">Указывает имя учетной записи автоматизации, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cde62-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cde62-120">-ResourceGroupName</span></span>
<span data-ttu-id="cde62-121">Указывает имя группы ресурсов, в которой этот командлет получает учетные записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="cde62-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cde62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde62-122">CommonParameters</span></span>
<span data-ttu-id="cde62-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cde62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde62-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde62-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde62-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cde62-125">INPUTS</span></span>

### <span data-ttu-id="cde62-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cde62-126">System.String</span></span>

## <span data-ttu-id="cde62-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cde62-127">OUTPUTS</span></span>

### <span data-ttu-id="cde62-128">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cde62-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="cde62-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="cde62-129">NOTES</span></span>

## <span data-ttu-id="cde62-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cde62-130">RELATED LINKS</span></span>

[<span data-ttu-id="cde62-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cde62-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="cde62-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cde62-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="cde62-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cde62-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


