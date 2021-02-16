---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229345"
---
# <span data-ttu-id="79a68-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="79a68-101">New-AzAttestation</span></span>

## <span data-ttu-id="79a68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a68-102">SYNOPSIS</span></span>
<span data-ttu-id="79a68-103">Создает проверку.</span><span class="sxs-lookup"><span data-stu-id="79a68-103">Creates an attestation</span></span>

## <span data-ttu-id="79a68-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="79a68-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79a68-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79a68-105">DESCRIPTION</span></span>
<span data-ttu-id="79a68-106">С New-AzAttestation создается атестация в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79a68-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="79a68-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="79a68-107">EXAMPLES</span></span>

### <span data-ttu-id="79a68-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79a68-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="79a68-109">Создайте новый экземпляр поставщика attestation с именем *pshtest4* с парой тегов и использованием доверия AAD для mastering TEE policy.</span><span class="sxs-lookup"><span data-stu-id="79a68-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="79a68-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="79a68-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="79a68-111">Создайте новый экземпляр поставщика attestation с именем *pshtest3,* который использует isoladed trust для mastering TEE policy посредством указания набора надежных ключей подписи с помощью PEM-файла.</span><span class="sxs-lookup"><span data-stu-id="79a68-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="79a68-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79a68-112">PARAMETERS</span></span>

### <span data-ttu-id="79a68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a68-113">-DefaultProfile</span></span>
<span data-ttu-id="79a68-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79a68-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a68-115">-Location</span><span class="sxs-lookup"><span data-stu-id="79a68-115">-Location</span></span>
<span data-ttu-id="79a68-116">Определяет регион Azure, в котором нужно создать поставщика для проверки.</span><span class="sxs-lookup"><span data-stu-id="79a68-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="79a68-117">Используйте команду Get-AzResourceProvider с параметром ProviderNamespace, чтобы увидеть ваши варианты.</span><span class="sxs-lookup"><span data-stu-id="79a68-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="79a68-118">-Name</span><span class="sxs-lookup"><span data-stu-id="79a68-118">-Name</span></span>
<span data-ttu-id="79a68-119">Указывает имя созда создаемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="79a68-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="79a68-120">Имя может быть любым сочетанием букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="79a68-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="79a68-121">Имя должно начинаться с буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="79a68-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="79a68-122">Имя должно быть универсальным.</span><span class="sxs-lookup"><span data-stu-id="79a68-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a68-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="79a68-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="79a68-124">Набор ключей надежных подписей для политики выдачи в одном файле сертификата.</span><span class="sxs-lookup"><span data-stu-id="79a68-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a68-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a68-125">-ResourceGroupName</span></span>
<span data-ttu-id="79a68-126">Указывает имя существующей группы ресурсов, в которой нужно создать проверку.</span><span class="sxs-lookup"><span data-stu-id="79a68-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="79a68-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="79a68-127">-Tag</span></span>
<span data-ttu-id="79a68-128">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="79a68-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a68-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79a68-129">-Confirm</span></span>
<span data-ttu-id="79a68-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a68-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a68-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a68-131">-WhatIf</span></span>
<span data-ttu-id="79a68-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a68-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a68-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="79a68-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a68-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a68-134">CommonParameters</span></span>
<span data-ttu-id="79a68-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a68-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a68-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79a68-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a68-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79a68-137">INPUTS</span></span>

### <span data-ttu-id="79a68-138">System.String</span><span class="sxs-lookup"><span data-stu-id="79a68-138">System.String</span></span>

### <span data-ttu-id="79a68-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="79a68-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="79a68-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79a68-140">OUTPUTS</span></span>

### <span data-ttu-id="79a68-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="79a68-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="79a68-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="79a68-142">NOTES</span></span>

## <span data-ttu-id="79a68-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79a68-143">RELATED LINKS</span></span>
