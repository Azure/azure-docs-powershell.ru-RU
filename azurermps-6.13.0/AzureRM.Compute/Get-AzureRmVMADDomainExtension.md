---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 398cc4b8f23ca5296aec741eb720833f589b0e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561056"
---
# <span data-ttu-id="d79bc-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d79bc-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="d79bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d79bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d79bc-103">Получает сведения о расширении доменных имен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d79bc-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d79bc-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d79bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d79bc-105">DESCRIPTION</span></span>
<span data-ttu-id="d79bc-106">Командлет **Get-AzureRmVMADDomainExtension** получает сведения об указанном расширении домена Azure Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="d79bc-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="d79bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d79bc-107">EXAMPLES</span></span>

## <span data-ttu-id="d79bc-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d79bc-108">PARAMETERS</span></span>

### <span data-ttu-id="d79bc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79bc-109">-DefaultProfile</span></span>
<span data-ttu-id="d79bc-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d79bc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79bc-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d79bc-111">-Name</span></span>
<span data-ttu-id="d79bc-112">Указывает имя расширения домена.</span><span class="sxs-lookup"><span data-stu-id="d79bc-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="d79bc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79bc-113">-ResourceGroupName</span></span>
<span data-ttu-id="d79bc-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d79bc-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d79bc-115">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="d79bc-115">-Status</span></span>
<span data-ttu-id="d79bc-116">Указывает на то, что этот командлет получает представление экземпляра расширения домена.</span><span class="sxs-lookup"><span data-stu-id="d79bc-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="d79bc-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="d79bc-117">-VMName</span></span>
<span data-ttu-id="d79bc-118">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d79bc-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="d79bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79bc-119">CommonParameters</span></span>
<span data-ttu-id="d79bc-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d79bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79bc-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79bc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79bc-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d79bc-122">INPUTS</span></span>

### <span data-ttu-id="d79bc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d79bc-123">System.String</span></span>

### <span data-ttu-id="d79bc-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d79bc-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d79bc-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d79bc-125">OUTPUTS</span></span>

### <span data-ttu-id="d79bc-126">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d79bc-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="d79bc-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d79bc-127">NOTES</span></span>

## <span data-ttu-id="d79bc-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d79bc-128">RELATED LINKS</span></span>

[<span data-ttu-id="d79bc-129">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="d79bc-129">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


