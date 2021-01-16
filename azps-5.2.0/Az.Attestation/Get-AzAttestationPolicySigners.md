---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicysigners
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicySigners.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicySigners.md
ms.openlocfilehash: f9635a4958d0daefdba075340f66af832bd2b168
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406687"
---
# <span data-ttu-id="8a088-101">Get-AzAttestationPolicySigners</span><span class="sxs-lookup"><span data-stu-id="8a088-101">Get-AzAttestationPolicySigners</span></span>

## <span data-ttu-id="8a088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a088-102">SYNOPSIS</span></span>
<span data-ttu-id="8a088-103">Получает доверенных подписателей политики из клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="8a088-103">Gets the trusted policy signers from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="8a088-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8a088-104">SYNTAX</span></span>

### <span data-ttu-id="8a088-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a088-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicySigners [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a088-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a088-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicySigners [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a088-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a088-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicySigners [-Location] <String> [-DefaultProvider]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a088-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a088-108">DESCRIPTION</span></span>
<span data-ttu-id="8a088-109">Этот Get-AzAttestationPolicySigners получает доверенных подписателей политики от клиента в Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="8a088-109">The Get-AzAttestationPolicySigners cmdlet gets the trusted policy signers from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="8a088-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8a088-110">EXAMPLES</span></span>

### <span data-ttu-id="8a088-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a088-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicySigners -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                          
CertificateCount : 0
Jwt              : eyJhbGciOiAiUlMyNTYiLCAiamt1IjogImh0dHBzOi8vcHNodGVzdC51cy5hdHRlc3QuYXp1cmUubmV0L2NlcnRzIiwgImtpZCI6ICJrdlB4aUJlemk4RGJsQVY0WE5nNG5wVjlocE5WTnRqS0NQTlZZUjRuRVJzPSIsICJ0eXAiOiAiSldUIn0.eyJhYXMtcG9saWN5Q2VydGlmaWNhdGVzIjogeyJrZXlzIjogW119LCAiZXhwIjogMTU4NDM5NDgxOSwgImlhdCI6IDE1ODQzOTEyMTksICJpc3MiOiAiaHR0cHM6Ly9wc2h0ZXN0LnVzLmF0dGVzdC5henVyZS5uZXQiLCAibmJmIjogMTU4NDM5MTIxOX0.hXDejUE2Tfbnvy0RN4ONyxtg2NTEmHKz7wOJIY2YhF43MUJQYgh7TREE3BAMl93mQIO9px2HNvo_MSzNhDRmCMvZt6tUdC8Gw1xK40w2nqngvfmTONOcKskSXUVc1Igk2C47cuCQjB1W8t2qdCrwpR4UTEGdidyGlb7NFkAaFMOK119H1c0DQ7LSpY0bqodrVDW1DNa0LOFLxL3DwxqkRF-itk
duZJn9aqlkrgIPPSE_kdNUUURjpx3F6eCEONsdtu8zfj76v7Yb6Oyf70rh8EOyVdEu2wwmfg9ASZnooANwo7C6o68ESpfvi6DHPTyBsD0rgysVsNYtkS0tuXNj3A
Algorithm        : RS256
JKU              : https://pshtest.us.attest.azure.net/certs
Certificates     : {}
```

<span data-ttu-id="8a088-112">Получает доверенных подписателей для поставщика attestation Provider *pshtest* в группе ресурсов *psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="8a088-112">Gets the trusted policy signers for the Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>  <span data-ttu-id="8a088-113">Обратите внимание, что для этого поставщика проверки нет доверенных подписок.</span><span class="sxs-lookup"><span data-stu-id="8a088-113">Note that there are no trusted signers for this Attestation Provider.</span></span>

### <span data-ttu-id="8a088-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8a088-114">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicySigners -Name pshtest2 -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                         
CertificateCount : 1
Jwt              : eyJhbGciOiAiUlMyNTYiLCAiamt1IjogImh0dHBzOi8vcHNodGVzdDIudXMuYXR0ZXN0LmF6dXJlLm5ldC9jZXJ0cyIsICJraWQiOiAiL09KMXJ0U0hkbFJnR1VqMGVuTEl5bDhLeHQ3NHZYdmJLTW9VbmFZMlNJRT0iLCAidHlwIjogIkpXVCJ9.eyJhYXMtcG9saWN5Q2VydGlmaWNhdGVzIjogeyJrZXlzIjogW3siYWxnIjogIlJTMjU2IiwgImt0eSI6ICJSU0EiLCAidXNlIjogInNpZyIsICJ4NWMiOiBbIk1JSURMRENDQWhTZ0F3SUJBZ0lJYStGTE1oT1ZkMFF3RFFZSktvWklodmNOQVFFTEJRQXdGekVWTUJNR0ExVUVBd3dNVFdGaFZHVnpkRU5sY25ReE1DQVhEVEl3TURNd016QXdNREF3TUZvWUR6SXdOekF3TXpBek1EQXdNREF3V2pBWE1SVXdFd1lEVlFRRERBeE5ZV0ZVWlhOMFEyVnlkREV3Z2dFaU1BMEdDU3FHU0liM0RRRUJBUVVBQTRJQkR3QXdnZ0VLQW9JQkFRQ3BidzRLeHJhME05OE9RNUMzQkk3Uk9BS2k4dnlRNTF5eWJoUi9saTJDd1Y4WkVJZmVZSEJMMFM5UC9naVQ2VTlZRkNtNEw3c2hGTm5kYTBJcG5zeTZSaFhCUnRYampZdVR1SlcxTk01SVh0OVFJMEtkUUNQbG5VVlNnb2UzdW9pQ0l6S25HU1Nka0MrU25nblVveDFsVnVRNEpLSmtLUXBubTFCekgzTGNzUEFnQUJwYTloVnlieG9XUHU4c2tEek1TSVFZVzMxemVYVkxZdlprZmxoTWttNFZLby9DUWpYNXJWTFNXeVZWa1YrOUhDQjlVQk1HMExiNmhldWZTQTVKTE5mR2taY0kwNHBHRmFqVzZnVUJkcmJnM2R4V0s5VzdKUVZYT05maEJ6NkE2bWM1a0wxRUtLNWhIc2dnekdYeEdLWmhwWU5JSDNiek52eTNrUUFQQWdNQkFBR2plakI0TUVZR0ExVWRJd1EvTUQyQUZIWnBTaFI4UUlRMGFzZy9Yb1NwR2hNOURGN25vUnVrR1RBWE1SVXdFd1lEVlFRRERBeE5ZV0ZVWlhOMFEyVnlkREdDQ0d2aFN6SVRsWGRFTUIwR0ExVWREZ1FXQkJSMmFVb1VmRUNFTkdySVAxNkVxUm9UUFF4ZTV6QVBCZ05WSFJNQkFmOEVCVEFEQVFIL01BMEdDU3FHU0liM0RRRUJDd1VBQTRJQkFRQVFpWXpFeUtVbDlkSWVUVGZnTVpBWEo0V0NFZXpFN2FRcHd2QnU5Rkk0MXN4L1pzbEV2RVFvTDVWNTZTQVhQZCtTOWdlZnVJNjFuZ056OTl5RTlrZGgrOWxmVTJVTU1tdXFCdVFWaWI5RzBKakllYVNHM1J2OGVyRXNGMUUrbXhjbzRtVGVEdUdLUklmN1dHNnNYZjZ5b2N1U0FVaEV2emM5NzZTSUNJLzQxclZEVkg5bnFJdS9LUnZleHpWcFJqZ1EzWlVnMTMydmVnb2djNjc1UndreTJHckxrZDBJN015bGcwZVIyamd1ZndLcTVBbnZ1YTlzRFJyUUpLUCtqclpmcWpiOEpoZ2VsUEtLVXl4S1JIS1Z6QUxzQ3JHTkRQS0ozVDlsWUhmZmFuWE9JeEpnTDExcDNBMmVMUWtWN3BMdEpUenhrb1lDZFZKdTNmbDZJNWVsIl19XX0sICJleHAiOiAxNTg0Mzk1MTE5LCAiaWF0IjogMTU4NDM5MTUxOSwgImlzcyI6ICJodHRwczovL3BzaHRlc3QyLnVzLmF0dGVzdC5henVyZS5uZXQiLCAibmJmIjogMTU4NDM5MTUxOX0Irkd3eNG7jD-fJThxBKURjjSlsfbRgOnOvN_nI8ukH-VvpaYIKGgk74iuefWhPYQJr--mAUT2IaEqcBGXvRV6K4oDUXUHn7iCNL1aIWzQ4udTrFVChNTUjEH4x1tmyDLC04SBeoi_yP5R0Bfijb51qnKwSU6ppuKTTletpzFztib2MN_RUQidHjuaeivMECJPRu5Bit2DbLRObokMRRY-rftcxPf7rLr1mK_4WUbRjIKT_ic03qWcqY0lakwC3MdFV9xQsvCH7-sizgJShSIOIS9pHrRp6YIEyG8LoF6Kj9aL-imNTUZ2IjwxtDJOmnhXh56pYjzQNpW_bzQlOeNaA
Algorithm        : RS256
JKU              : https://pshtest2.us.attest.azure.net/certs
Certificates     : {{
                     "alg": "RS256",
                     "kty": "RSA",
                     "use": "sig",
                     "x5c": ["MIIDLDCCAhSgAwIBAgIIa+FLMhOVd0QwDQYJKoZIhvcNAQELBQAwFzEVMBMGA1UEAwwMTWFhVGVzdENlcnQxMCAXDTIwMDMwMzAwMDAwMFoYDzIwNzAwMzAzMDAwMDAwWjAXMRUwEwYDVQQDDAxNYWFUZXN0Q2VydDEwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCpbw4Kxra0M98OQ5C3BI7ROAKi8vyQ51yybhR/li2CwV8ZEIfeYHBL0S9P/giT6U9YFCm4L7shFNnda0Ipnsy6RhXBRtXjjYuTuJW1NM5IXt9QI0KdQCPlnUVSgoe3uoiCIzKnGSSdkC+SngnUox1lVuQ4JKJkKQpnm1BzH3LcsPAgABpa9hVybxoWPu8skDzMSIQYW31zeXVLYvZkflhMkm4VKo/CQjX5rVLSWyVVkV+9HCB9UBMG0Lb6heufSA5JLNfGkZcI04pGFajW6gUBdrbg3dxWK9W7JQVXONfhBz6A6mc5kL1EKK5hHsggzGXxGKZhpYNIH3bzNvy3kQAPAgMBAAGjejB4MEYGA1UdIwQ/MD2AFHZpShR8QIQ0asg/XoSpGhM9DF7noRukGTAXMRUwEwYDVQQDDAxNYWFUZXN0Q2VydDGCCGvhSzITlXdEMB0GA1UdDgQWBBR2aUoUfECENGrIP16EqRoTPQxe5zAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3DQEBCwUAA4IBAQAQiYzEyKUl9dIeTTfgMZAXJ4WCEezE7aQpwvBu9FI41sx/ZslEvEQoL5V56SAXPd+S9gefuI61ngNz99yE9kdh+9lfU2UMMmuqBuQVib9G0JjIeaSG3Rv8erEsF1E+mxco4mTeDuGKRIf7WG6sXf6yocuSAUhEvzc976SICI/41rVDVH9nqIu/KRvexzVpRjgQ3ZUg132vegogc675Rwky2GrLkd0I7Mylg0eR2jgufwKq5Anvua9sDRrQJKP+jrZfqjb8JhgelPKKUyxKRHKVzALsCrGNDPKJ3T9lYHffanXOIxJgL11p3A2eLQkV7pLtJTzxkoYCdVJu3fl6I5el"]
                   }}
```

<span data-ttu-id="8a088-115">Подписывает доверенных подписателей для поставщика attestation Provider *pshtest2* в группе ресурсов *psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="8a088-115">Gets the trusted policy signers for the Attestation Provider *pshtest2* in Resource Group *psh-test-rg*.</span></span>  <span data-ttu-id="8a088-116">Обратите внимание, что для этого поставщика attestation имеется один надежный подписыватель.</span><span class="sxs-lookup"><span data-stu-id="8a088-116">Note that there is one trusted signer for this Attestation Provider.</span></span>

### <span data-ttu-id="8a088-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8a088-117">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestationPolicySigners -DefaultProvider -Location "Central US"
CertificateCount : 0
Jwt              : eyJhbGciOiAiUlMyNTYiLCAiamt1IjogImh0dHBzOi8vc2hhcmVkZXVzLmV1cy50ZXN0LmF0dGVzdC5henVyZS5uZXQvY2VydHMi
                   LCAia2lkIjogIlhodGZtZlR0bS9MNnhUUkU2RGoxc3BTVkpSRnAwcXdyTjNRem9RWHJwR0E9IiwgInR5cCI6ICJKV1QifQ.eyJhY
                   XMtcG9saWN5Q2VydGlmaWNhdGVzIjogeyJrZXlzIjogW119LCAiZXhwIjogMTU5Mzc1ODEyOCwgImlhdCI6IDE1OTM3NTQ1MjgsI
                   CJpc3MiOiAiaHR0cHM6Ly9zaGFyZWRldXMuZXVzLnRlc3QuYXR0ZXN0LmF6dXJlLm5ldCIsICJtYWEtcG9saWN5Q2VydGlmaWNhd
                   GVzIjogeyJrZXlzIjogW119LCAibmJmIjogMTU5Mzc1NDUyOH0.C1FPzJVuAQQszL1s-5FpiZf4YDF7VD6cYnoy0S9QFAQYlJOy-
                   PX00GT_uCnOHKzPvhwQ-doiQCkEhIRpA6coK9gEU4k_R4KK5kmtWZEpzDGo2M-8ScIsVQlN0-nITfMk4kf4nRZgiqWSr_X7nuWCD
                   7Ddhj0OrKWK_6Cz6WlktGrjdhozU0-HNNTy6DKWcLB3cubPY9j6L9Uyvu4uO5m1QjN_Cn4G_6Zq21aM89kOcUzDgpHYralrNXkKH
                   3XBRKfGcQqatJky8Tq3s5Kd-0TRokOsekH681fMTFv_K2R6ORxOPoh7h-dX7LysmSGqmX_7GqhAgTGGXBaGekO6BNRe1A
Algorithm        : RS256
JKU              : https://sharedcus.cus.attest.azure.net/certs
Certificates     : {}
```

<span data-ttu-id="8a088-118">Подписывает доверенных подписателей поставщика по умолчанию для проверки attestation в Центре *нахождения США.*</span><span class="sxs-lookup"><span data-stu-id="8a088-118">Gets the trusted policy signers for the Attestation Default Provider in Location *Central US*.</span></span>  <span data-ttu-id="8a088-119">Обратите внимание, что надежных подписателей для поставщика по умолчанию для проверки attestation нет.</span><span class="sxs-lookup"><span data-stu-id="8a088-119">Note that there are no trusted signers for Attestation Default Provider.</span></span>

## <span data-ttu-id="8a088-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a088-120">PARAMETERS</span></span>

### <span data-ttu-id="8a088-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a088-121">-DefaultProfile</span></span>
<span data-ttu-id="8a088-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a088-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a088-123">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="8a088-123">-DefaultProvider</span></span>
<span data-ttu-id="8a088-124">Указывает, что это запрос к поставщику услуг проверки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a088-124">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a088-125">-Location</span><span class="sxs-lookup"><span data-stu-id="8a088-125">-Location</span></span>
<span data-ttu-id="8a088-126">Определяет расположение поставщика для проверки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a088-126">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a088-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8a088-127">-Name</span></span>
<span data-ttu-id="8a088-128">Указывает имя поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="8a088-128">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="8a088-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a088-129">-ResourceGroupName</span></span>
<span data-ttu-id="8a088-130">Указывает имя группы ресурсов для поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="8a088-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="8a088-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a088-131">-ResourceId</span></span>
<span data-ttu-id="8a088-132">Определяет ИД ресурса поставщика услуг проверки.</span><span class="sxs-lookup"><span data-stu-id="8a088-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="8a088-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a088-133">CommonParameters</span></span>
<span data-ttu-id="8a088-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a088-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a088-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a088-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a088-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a088-136">INPUTS</span></span>

### <span data-ttu-id="8a088-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8a088-137">System.String</span></span>

## <span data-ttu-id="8a088-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8a088-138">OUTPUTS</span></span>

### <span data-ttu-id="8a088-139">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="8a088-139">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="8a088-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8a088-140">NOTES</span></span>

## <span data-ttu-id="8a088-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a088-141">RELATED LINKS</span></span>