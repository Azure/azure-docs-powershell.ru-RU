---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 0c36f5fb87e3d247a48031bdc735c077a577ac27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072735"
---
# <span data-ttu-id="5247e-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="5247e-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="5247e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5247e-102">SYNOPSIS</span></span>
<span data-ttu-id="5247e-103">Получает политику из клиента в аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="5247e-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="5247e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5247e-104">SYNTAX</span></span>

### <span data-ttu-id="5247e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5247e-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5247e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5247e-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5247e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5247e-107">DESCRIPTION</span></span>
<span data-ttu-id="5247e-108">Командлет Get-AzAttestationPolicy получает политику из клиента в аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="5247e-108">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="5247e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5247e-109">EXAMPLES</span></span>

### <span data-ttu-id="5247e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5247e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

<span data-ttu-id="5247e-111">Возвращает политику для поставщика аттестации *pshtest* для надежной среды выполнения типа *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="5247e-111">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="5247e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5247e-112">PARAMETERS</span></span>

### <span data-ttu-id="5247e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5247e-113">-DefaultProfile</span></span>
<span data-ttu-id="5247e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5247e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5247e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5247e-115">-Name</span></span>
<span data-ttu-id="5247e-116">Указывает имя клиента.</span><span class="sxs-lookup"><span data-stu-id="5247e-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="5247e-117">Этот командлет получает политику аттестации для клиента, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="5247e-117">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5247e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5247e-118">-ResourceGroupName</span></span>
<span data-ttu-id="5247e-119">Указывает имя группы ресурсов для поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="5247e-119">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5247e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5247e-120">-ResourceId</span></span>
<span data-ttu-id="5247e-121">Указывает ResourceID поставщика аттестации.</span><span class="sxs-lookup"><span data-stu-id="5247e-121">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5247e-122">-Надежной среды выполнения</span><span class="sxs-lookup"><span data-stu-id="5247e-122">-Tee</span></span>
<span data-ttu-id="5247e-123">Указывает тип надежной среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="5247e-123">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="5247e-124">Поддерживаются четыре типа среды: SgxEnclave, OpenEnclave, CyResComponent и VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="5247e-124">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5247e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5247e-125">-Confirm</span></span>
<span data-ttu-id="5247e-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5247e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5247e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5247e-127">-WhatIf</span></span>
<span data-ttu-id="5247e-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5247e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5247e-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5247e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5247e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5247e-130">CommonParameters</span></span>
<span data-ttu-id="5247e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5247e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5247e-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5247e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5247e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5247e-133">INPUTS</span></span>

### <span data-ttu-id="5247e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5247e-134">System.String</span></span>

## <span data-ttu-id="5247e-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5247e-135">OUTPUTS</span></span>

### <span data-ttu-id="5247e-136">Microsoft. Azure. Commands. аттестация. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="5247e-136">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="5247e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5247e-137">NOTES</span></span>

## <span data-ttu-id="5247e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5247e-138">RELATED LINKS</span></span>
