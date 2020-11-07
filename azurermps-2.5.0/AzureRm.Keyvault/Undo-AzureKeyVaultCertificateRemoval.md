---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultcertificateremoval
schema: 2.0.0
ms.openlocfilehash: 493d4bcd641e8132bffd49100a04732759ce7e91
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913871"
---
# <span data-ttu-id="035e2-101">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="035e2-101">Undo-AzureKeyVaultCertificateRemoval</span></span>

## <span data-ttu-id="035e2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="035e2-102">SYNOPSIS</span></span>
<span data-ttu-id="035e2-103">Восстановление удаленного сертификата из хранилища ключей в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="035e2-103">Recovers a deleted certificate in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="035e2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="035e2-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultCertificateRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="035e2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="035e2-105">DESCRIPTION</span></span>
<span data-ttu-id="035e2-106">Командлет **Undo-AzureKeyVaultCertificateRemoval** восстановит ранее удаленный сертификат.</span><span class="sxs-lookup"><span data-stu-id="035e2-106">The **Undo-AzureKeyVaultCertificateRemoval** cmdlet will recover a previously deleted certificate.</span></span>
<span data-ttu-id="035e2-107">Восстановленный сертификат будет активен и может использоваться для всех операций.</span><span class="sxs-lookup"><span data-stu-id="035e2-107">The recovered certificate will be active and can be used for all operations.</span></span>
<span data-ttu-id="035e2-108">Для выполнения этой операции вызывающему объекту должно быть предоставлено разрешение "Recover".</span><span class="sxs-lookup"><span data-stu-id="035e2-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="035e2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="035e2-109">EXAMPLES</span></span>

### <span data-ttu-id="035e2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="035e2-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultCertificateRemoval -VaultName 'MyKeyVault' -Name 'MyCertificate'
```

<span data-ttu-id="035e2-111">Эта команда восстановит сертификат "MyCertificate", который ранее был удален, в активное и пригодное для использования состояние.</span><span class="sxs-lookup"><span data-stu-id="035e2-111">This command will recover the certificate 'MyCertificate' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="035e2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="035e2-112">PARAMETERS</span></span>

### <span data-ttu-id="035e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035e2-113">-DefaultProfile</span></span>
<span data-ttu-id="035e2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="035e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="035e2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="035e2-115">-Name</span></span>
<span data-ttu-id="035e2-116">Имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="035e2-116">Certificate name.</span></span>
<span data-ttu-id="035e2-117">Командлет создает полное доменное имя сертификата из имени хранилища, выбранной в данный момент среды и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="035e2-117">Cmdlet constructs the FQDN of a certificate from vault name, currently selected environment and certificate name.</span></span>

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

### <span data-ttu-id="035e2-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="035e2-118">-VaultName</span></span>
<span data-ttu-id="035e2-119">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="035e2-119">Vault name.</span></span>
<span data-ttu-id="035e2-120">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="035e2-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="035e2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="035e2-121">-Confirm</span></span>
<span data-ttu-id="035e2-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="035e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="035e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="035e2-123">-WhatIf</span></span>
<span data-ttu-id="035e2-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="035e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="035e2-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="035e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="035e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035e2-126">CommonParameters</span></span>
<span data-ttu-id="035e2-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="035e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035e2-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035e2-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="035e2-129">INPUTS</span></span>

### <span data-ttu-id="035e2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="035e2-130">System.String</span></span>

## <span data-ttu-id="035e2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="035e2-131">OUTPUTS</span></span>

### <span data-ttu-id="035e2-132">Microsoft. Azure. Commands. KeyVault. Models. Certificate</span><span class="sxs-lookup"><span data-stu-id="035e2-132">Microsoft.Azure.Commands.KeyVault.Models.Certificate</span></span>

## <span data-ttu-id="035e2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="035e2-133">NOTES</span></span>

## <span data-ttu-id="035e2-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="035e2-134">RELATED LINKS</span></span>

[<span data-ttu-id="035e2-135">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="035e2-135">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="035e2-136">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="035e2-136">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)
