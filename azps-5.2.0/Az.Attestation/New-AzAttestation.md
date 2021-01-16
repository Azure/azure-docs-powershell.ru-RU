---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406668"
---
# <span data-ttu-id="18013-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="18013-101">New-AzAttestation</span></span>

## <span data-ttu-id="18013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18013-102">SYNOPSIS</span></span>
<span data-ttu-id="18013-103">Создает проверку.</span><span class="sxs-lookup"><span data-stu-id="18013-103">Creates an attestation</span></span>

## <span data-ttu-id="18013-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="18013-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18013-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18013-105">DESCRIPTION</span></span>
<span data-ttu-id="18013-106">С New-AzAttestation создается атестация в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="18013-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="18013-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="18013-107">EXAMPLES</span></span>

### <span data-ttu-id="18013-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="18013-108">Example 1</span></span>
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

<span data-ttu-id="18013-109">Создайте новый экземпляр поставщика attestation с именем *pshtest4* с парой тегов и использованием доверия AAD для mastering TEE policy.</span><span class="sxs-lookup"><span data-stu-id="18013-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="18013-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="18013-110">Example 2</span></span>
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

<span data-ttu-id="18013-111">Создайте новый экземпляр поставщика attestation с именем *pshtest3,* который использует isoladed trust для mastering TEE policy посредством указания набора доверенных ключей подписи с помощью PEM-файла.</span><span class="sxs-lookup"><span data-stu-id="18013-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="18013-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18013-112">PARAMETERS</span></span>

### <span data-ttu-id="18013-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18013-113">-DefaultProfile</span></span>
<span data-ttu-id="18013-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18013-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18013-115">-Location</span><span class="sxs-lookup"><span data-stu-id="18013-115">-Location</span></span>
<span data-ttu-id="18013-116">Определяет регион Azure, в котором нужно создать поставщика для проверки.</span><span class="sxs-lookup"><span data-stu-id="18013-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="18013-117">Используйте команду Get-AzResourceProvider с параметром ProviderNamespace, чтобы увидеть ваши варианты.</span><span class="sxs-lookup"><span data-stu-id="18013-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="18013-118">-Name</span><span class="sxs-lookup"><span data-stu-id="18013-118">-Name</span></span>
<span data-ttu-id="18013-119">Указывает имя созда создаемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="18013-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="18013-120">Имя может быть любым сочетанием букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="18013-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="18013-121">Имя должно начинаться с буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="18013-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="18013-122">Имя должно быть универсальным.</span><span class="sxs-lookup"><span data-stu-id="18013-122">The name must be universally unique.</span></span>

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

### <span data-ttu-id="18013-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="18013-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="18013-124">Набор надежных ключей подписи для политики выдачи в одном файле сертификата.</span><span class="sxs-lookup"><span data-stu-id="18013-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="18013-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18013-125">-ResourceGroupName</span></span>
<span data-ttu-id="18013-126">Указывает имя существующей группы ресурсов, в которой нужно создать проверку.</span><span class="sxs-lookup"><span data-stu-id="18013-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="18013-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="18013-127">-Tag</span></span>
<span data-ttu-id="18013-128">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="18013-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="18013-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18013-129">-Confirm</span></span>
<span data-ttu-id="18013-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="18013-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18013-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18013-131">-WhatIf</span></span>
<span data-ttu-id="18013-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18013-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18013-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="18013-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18013-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18013-134">CommonParameters</span></span>
<span data-ttu-id="18013-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18013-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18013-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18013-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18013-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18013-137">INPUTS</span></span>

### <span data-ttu-id="18013-138">System.String</span><span class="sxs-lookup"><span data-stu-id="18013-138">System.String</span></span>

### <span data-ttu-id="18013-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="18013-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="18013-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="18013-140">OUTPUTS</span></span>

### <span data-ttu-id="18013-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="18013-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="18013-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="18013-142">NOTES</span></span>

## <span data-ttu-id="18013-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18013-143">RELATED LINKS</span></span>
