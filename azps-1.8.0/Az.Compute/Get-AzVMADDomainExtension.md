---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 2ec4ec1898e79fd7f7f35a406f2a99f9dd2da6fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731353"
---
# <span data-ttu-id="cecd0-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cecd0-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="cecd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cecd0-102">SYNOPSIS</span></span>
<span data-ttu-id="cecd0-103">Получает сведения о расширении доменных имен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cecd0-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="cecd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cecd0-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cecd0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cecd0-105">DESCRIPTION</span></span>
<span data-ttu-id="cecd0-106">Командлет **Get-AzVMADDomainExtension** получает сведения об указанном расширении домена Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="cecd0-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="cecd0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cecd0-107">EXAMPLES</span></span>

## <span data-ttu-id="cecd0-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cecd0-108">PARAMETERS</span></span>

### <span data-ttu-id="cecd0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cecd0-109">-DefaultProfile</span></span>
<span data-ttu-id="cecd0-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cecd0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cecd0-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cecd0-111">-Name</span></span>
<span data-ttu-id="cecd0-112">Указывает имя расширения домена.</span><span class="sxs-lookup"><span data-stu-id="cecd0-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecd0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cecd0-113">-ResourceGroupName</span></span>
<span data-ttu-id="cecd0-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cecd0-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cecd0-115">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="cecd0-115">-Status</span></span>
<span data-ttu-id="cecd0-116">Указывает на то, что этот командлет получает представление экземпляра расширения домена.</span><span class="sxs-lookup"><span data-stu-id="cecd0-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecd0-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="cecd0-117">-VMName</span></span>
<span data-ttu-id="cecd0-118">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cecd0-118">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecd0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cecd0-119">CommonParameters</span></span>
<span data-ttu-id="cecd0-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cecd0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cecd0-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cecd0-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cecd0-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cecd0-122">INPUTS</span></span>

### <span data-ttu-id="cecd0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cecd0-123">System.String</span></span>

### <span data-ttu-id="cecd0-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cecd0-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cecd0-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cecd0-125">OUTPUTS</span></span>

### <span data-ttu-id="cecd0-126">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="cecd0-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="cecd0-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="cecd0-127">NOTES</span></span>

## <span data-ttu-id="cecd0-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cecd0-128">RELATED LINKS</span></span>

[<span data-ttu-id="cecd0-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="cecd0-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


