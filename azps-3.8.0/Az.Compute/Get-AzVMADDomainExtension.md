---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: ca6b3d4863629aa94585db9850042fff4165dd10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075066"
---
# <span data-ttu-id="d4e25-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d4e25-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="d4e25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4e25-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e25-103">Получает сведения о расширении доменных имен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d4e25-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="d4e25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4e25-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4e25-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4e25-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e25-106">Командлет **Get-AzVMADDomainExtension** получает сведения об указанном расширении домена Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="d4e25-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="d4e25-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4e25-107">EXAMPLES</span></span>

## <span data-ttu-id="d4e25-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4e25-108">PARAMETERS</span></span>

### <span data-ttu-id="d4e25-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e25-109">-DefaultProfile</span></span>
<span data-ttu-id="d4e25-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4e25-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4e25-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d4e25-111">-Name</span></span>
<span data-ttu-id="d4e25-112">Указывает имя расширения домена.</span><span class="sxs-lookup"><span data-stu-id="d4e25-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="d4e25-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e25-113">-ResourceGroupName</span></span>
<span data-ttu-id="d4e25-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4e25-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d4e25-115">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="d4e25-115">-Status</span></span>
<span data-ttu-id="d4e25-116">Указывает на то, что этот командлет получает представление экземпляра расширения домена.</span><span class="sxs-lookup"><span data-stu-id="d4e25-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="d4e25-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="d4e25-117">-VMName</span></span>
<span data-ttu-id="d4e25-118">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d4e25-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="d4e25-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e25-119">CommonParameters</span></span>
<span data-ttu-id="d4e25-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4e25-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e25-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4e25-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e25-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4e25-122">INPUTS</span></span>

### <span data-ttu-id="d4e25-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e25-123">System.String</span></span>

### <span data-ttu-id="d4e25-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d4e25-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d4e25-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4e25-125">OUTPUTS</span></span>

### <span data-ttu-id="d4e25-126">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d4e25-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="d4e25-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4e25-127">NOTES</span></span>

## <span data-ttu-id="d4e25-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4e25-128">RELATED LINKS</span></span>

[<span data-ttu-id="d4e25-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d4e25-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


