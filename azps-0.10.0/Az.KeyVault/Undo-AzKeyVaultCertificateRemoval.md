---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultcertificateremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultCertificateRemoval.md
ms.openlocfilehash: 5757a9fb050d69cdf0ef0e648b0d446de1e3ee24
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910271"
---
# <span data-ttu-id="b4e98-101">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="b4e98-101">Undo-AzKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="b4e98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4e98-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e98-103">Восстановление удаленного сертификата из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b4e98-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

## <span data-ttu-id="b4e98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4e98-104">SYNTAX</span></span>

```
Undo-AzKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4e98-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e98-106">Командлет **Undo-AzKeyVaultCertificateRemoval** восстановит ранее удаленный сертификат.</span><span class="sxs-lookup"><span data-stu-id="b4e98-106">The **Undo-AzKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="b4e98-107">Восстановленный сертификат будет активен и может использоваться для всех операций.</span><span class="sxs-lookup"><span data-stu-id="b4e98-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="b4e98-108">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="b4e98-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b4e98-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4e98-109">EXAMPLES</span></span>

### <span data-ttu-id="b4e98-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4e98-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="b4e98-111">Эта команда восстановит сертификат "MyCertificate", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="b4e98-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b4e98-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4e98-112">PARAMETERS</span></span>

### <span data-ttu-id="b4e98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e98-113">-DefaultProfile</span></span>
<span data-ttu-id="b4e98-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b4e98-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e98-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4e98-115">-Name</span></span>
<span data-ttu-id="b4e98-116">Имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="b4e98-116">Certificate name.</span></span>
<span data-ttu-id="b4e98-117">Командлет создает полное доменное имя сертификата из имени хранилища, выбранной в данный момент среды и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="b4e98-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e98-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b4e98-118">-VaultName</span></span>
<span data-ttu-id="b4e98-119">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="b4e98-119">Vault name.</span></span>
<span data-ttu-id="b4e98-120">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="b4e98-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e98-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4e98-121">-Confirm</span></span>
<span data-ttu-id="b4e98-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b4e98-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e98-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e98-123">-WhatIf</span></span>
<span data-ttu-id="b4e98-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b4e98-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4e98-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b4e98-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e98-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e98-126">CommonParameters</span></span>
<span data-ttu-id="b4e98-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4e98-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e98-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e98-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e98-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4e98-129">INPUTS</span></span>

### <span data-ttu-id="b4e98-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b4e98-130">System.String</span></span>

## <span data-ttu-id="b4e98-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4e98-131">OUTPUTS</span></span>

### <span data-ttu-id="b4e98-132">Microsoft. Azure. Commands. KeyVault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="b4e98-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="b4e98-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4e98-133">NOTES</span></span>

## <span data-ttu-id="b4e98-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4e98-134">RELATED LINKS</span></span>

[<span data-ttu-id="b4e98-135">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b4e98-135">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="b4e98-136">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b4e98-136">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)
