---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: 7cddd6ab52774c6ae377ecddb6883d5019d6d7fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735122"
---
# <span data-ttu-id="8ab88-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ab88-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="8ab88-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ab88-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab88-103">Возвращает учетные записи автоматизации в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ab88-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab88-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ab88-104">SYNTAX</span></span>

### <span data-ttu-id="8ab88-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ab88-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ab88-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ab88-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ab88-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ab88-107">DESCRIPTION</span></span>
<span data-ttu-id="8ab88-108">Командлет **Get-AzureRmAutomationAccount** получает учетные записи службы автоматизации Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ab88-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>

<span data-ttu-id="8ab88-109">Дополнительные сведения об учетных записях автоматизации можно найти в командлете New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="8ab88-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="8ab88-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ab88-110">EXAMPLES</span></span>

### <span data-ttu-id="8ab88-111">Пример 1: получение всех учетных записей</span><span class="sxs-lookup"><span data-stu-id="8ab88-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="8ab88-112">Эта команда получает все учетные записи автоматизации в группе ресурсов с именем ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="8ab88-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="8ab88-113">Пример 2: получение учетной записи</span><span class="sxs-lookup"><span data-stu-id="8ab88-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="8ab88-114">Эта команда получает учетную запись автоматизации с именем ContosoAutomationAccount в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8ab88-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="8ab88-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ab88-115">PARAMETERS</span></span>

### <span data-ttu-id="8ab88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab88-116">-DefaultProfile</span></span>
<span data-ttu-id="8ab88-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8ab88-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab88-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ab88-118">-Name</span></span>
<span data-ttu-id="8ab88-119">Указывает имя учетной записи автоматизации, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8ab88-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab88-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab88-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ab88-121">Указывает имя группы ресурсов, в которой этот командлет получает учетные записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8ab88-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByAutomationAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab88-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab88-122">CommonParameters</span></span>
<span data-ttu-id="8ab88-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ab88-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab88-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ab88-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab88-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ab88-125">INPUTS</span></span>

### <span data-ttu-id="8ab88-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="8ab88-126">None</span></span>
<span data-ttu-id="8ab88-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8ab88-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ab88-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ab88-128">OUTPUTS</span></span>

### <span data-ttu-id="8ab88-129">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ab88-129">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="8ab88-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ab88-130">NOTES</span></span>

## <span data-ttu-id="8ab88-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ab88-131">RELATED LINKS</span></span>

[<span data-ttu-id="8ab88-132">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ab88-132">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="8ab88-133">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ab88-133">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="8ab88-134">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="8ab88-134">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


