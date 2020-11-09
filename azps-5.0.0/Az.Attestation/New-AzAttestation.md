---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315353"
---
# <span data-ttu-id="cc139-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="cc139-101">New-AzAttestation</span></span>

## <span data-ttu-id="cc139-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc139-102">SYNOPSIS</span></span>
<span data-ttu-id="cc139-103">Создание аттестации</span><span class="sxs-lookup"><span data-stu-id="cc139-103">Creates an attestation</span></span>

## <span data-ttu-id="cc139-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc139-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc139-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc139-105">DESCRIPTION</span></span>
<span data-ttu-id="cc139-106">Командлет New-AzAttestation создает аттестацию в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc139-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="cc139-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc139-107">EXAMPLES</span></span>

### <span data-ttu-id="cc139-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc139-108">Example 1</span></span>
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

<span data-ttu-id="cc139-109">Создайте новый экземпляр поставщика аттестации с именем *pshtest4* , используя пару тегов и указав для политики надежной среды выполнения Trust.</span><span class="sxs-lookup"><span data-stu-id="cc139-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="cc139-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cc139-110">Example 2</span></span>
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

<span data-ttu-id="cc139-111">Создайте новый экземпляр поставщика аттестации с именем *pshtest3* , который использует Isoladed Trust для политики главной настройки надежной среды выполнения, указав набор доверенных ключей подписи с помощью PEM-файла.</span><span class="sxs-lookup"><span data-stu-id="cc139-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="cc139-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc139-112">PARAMETERS</span></span>

### <span data-ttu-id="cc139-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc139-113">-DefaultProfile</span></span>
<span data-ttu-id="cc139-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc139-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc139-115">-Location</span><span class="sxs-lookup"><span data-stu-id="cc139-115">-Location</span></span>
<span data-ttu-id="cc139-116">Указывает область Azure, в которой нужно создать поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="cc139-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="cc139-117">Используйте командную Get-AzResourceProvider с параметром ProviderNamespace, чтобы просмотреть варианты выбора.</span><span class="sxs-lookup"><span data-stu-id="cc139-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="cc139-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc139-118">-Name</span></span>
<span data-ttu-id="cc139-119">Указывает имя создаваемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cc139-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="cc139-120">Имя может представлять собой любую комбинацию букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="cc139-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="cc139-121">Имя должно начинаться и заканчиваться на букву или цифру.</span><span class="sxs-lookup"><span data-stu-id="cc139-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="cc139-122">Имя должно быть универсальным уникальным.</span><span class="sxs-lookup"><span data-stu-id="cc139-122">The name must be universally unique.</span></span>

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

### <span data-ttu-id="cc139-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="cc139-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="cc139-124">Задает набор доверенных ключей подписывания для политики выдачи в одном файле сертификата.</span><span class="sxs-lookup"><span data-stu-id="cc139-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="cc139-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc139-125">-ResourceGroupName</span></span>
<span data-ttu-id="cc139-126">Указывает имя существующей группы ресурсов, в которой будет создана аттестация.</span><span class="sxs-lookup"><span data-stu-id="cc139-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="cc139-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="cc139-127">-Tag</span></span>
<span data-ttu-id="cc139-128">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc139-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="cc139-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc139-129">-Confirm</span></span>
<span data-ttu-id="cc139-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc139-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc139-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc139-131">-WhatIf</span></span>
<span data-ttu-id="cc139-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc139-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc139-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc139-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc139-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc139-134">CommonParameters</span></span>
<span data-ttu-id="cc139-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc139-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc139-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc139-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc139-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc139-137">INPUTS</span></span>

### <span data-ttu-id="cc139-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cc139-138">System.String</span></span>

### <span data-ttu-id="cc139-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cc139-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cc139-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc139-140">OUTPUTS</span></span>

### <span data-ttu-id="cc139-141">Microsoft. Azure. Commands. аттестация. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="cc139-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="cc139-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc139-142">NOTES</span></span>

## <span data-ttu-id="cc139-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc139-143">RELATED LINKS</span></span>
